# Temporary Email for Testing and API Workflows

Email is part of many critical product journeys: registration, address verification, passwordless sign-in, invitations, receipts, alerts, and account recovery. Testing those journeys with employee inboxes is slow, difficult to isolate, and likely to leave large amounts of test mail behind.

A disposable inbox provides a unique receiving address for each test while keeping test traffic separate from permanent accounts.

## Useful test cases

### Registration and verification

Create a new address, submit it through the signup form, wait for the verification message, and confirm that the expected code or link arrives. The full message should be checked when the exact wording, sender, or branding is part of the test.

### Magic links and passwordless sign-in

A temporary inbox can receive a one-time sign-in link without requiring a pool of managed test accounts. Treat the link as a credential while the test is running and avoid writing it to shared logs.

### Invitation workflows

Generate a different address for each role or organization. This makes it easier to confirm that invitations contain the correct tenant, role, expiry, and destination.

### Staging notifications

Use a dedicated domain or prefix to keep staging messages separate from production email. A private custom domain is preferable if test messages may contain internal details.

### Deliverability checks

A receiving inbox can verify that a message left the application and reached an external mail system. It cannot by itself prove broad deliverability across Gmail, Outlook, corporate filters, or regional providers, so use it as one signal rather than a complete deliverability test.

## Browser workflow

For manual QA, the GPTMail website and Chrome extension minimize context switching:

1. generate a fresh address;
2. paste or suggest it in the form being tested;
3. submit the flow;
4. watch the inbox or browser badge;
5. open the message and finish the verification step;
6. mark the test complete and let temporary retention remove the message.

Install the **[GPTMail Chrome extension](https://chromewebstore.google.com/detail/eplebonhkjiahfnoaiifngokamaipeoo)** for toolbar, side-panel, notification, and optional email-field assistance.

## API workflow

GPTMail also exposes an HTTP API for approved automated use. The live documentation at **[mail.chatgpt.org.uk/api](https://mail.chatgpt.org.uk/api)** is the source of truth for endpoints, request fields, quotas, and current response formats.

A reliable automated flow should:

1. obtain an API key through the supported process;
2. create or select a temporary address;
3. submit that address to the application under test;
4. poll the inbox at a reasonable interval with a clear timeout;
5. identify the expected message by sender, subject, timestamp, or test identifier;
6. retrieve the message details only when needed;
7. extract and validate the expected code or link;
8. stop polling immediately after success or timeout.

## Credential handling

Send API keys in the documented request header. Do not place a key in:

- a query string;
- client-side JavaScript shipped to untrusted users;
- public repositories;
- screenshots;
- analytics events;
- CI logs or test reports.

Use secret storage provided by the CI platform and limit access to the jobs that require it. Rotate a key if it is exposed.

## Polling without unnecessary load

Email delivery is asynchronous. Polling many times per second does not make the sender deliver faster and can cause rate limiting. A better strategy is:

- start with a short interval suitable for an interactive test;
- use backoff for longer waits;
- set an overall deadline;
- stop after the target email is found;
- avoid repeatedly downloading full message bodies when the inbox summary is enough.

Tests should report the difference between “message not delivered before the deadline” and “API request failed.” Those outcomes have different causes and require different debugging.

## Avoid flaky verification-code matching

Do not accept the first number found in any message. Match the expected sender and subject, prefer a message received after the test started, and validate the code format used by the application. Marketing email, dates, prices, and tracking identifiers can all contain numbers that look like one-time codes.

When possible, include a unique test identifier in the signup data or message template. Open the full message when automated extraction returns no result or an ambiguous result.

## Privacy and cleanup

Test email can still contain personal data, session links, and internal URLs. Use synthetic accounts, avoid real customer information, and prefer private-domain inboxes for non-public test environments. Temporary retention is useful, but it is not a substitute for careful test-data design.

## Start testing

- [Open GPTMail](https://mail.chatgpt.org.uk/)
- [Read the live API documentation](https://mail.chatgpt.org.uk/api)
- [Configure a custom domain](custom-domains-and-private-inboxes.md)
- [Review responsible-use guidance](how-temporary-email-works.md)
