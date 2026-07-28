# Verification Email Not Received? A Practical Checklist

A missing verification email does not always mean the temporary inbox is broken. The message passes through several independent systems: the website that sends it, the sender's email provider, DNS, the receiving domain, and the inbox interface. A delay or rejection at any stage can stop the code from appearing.

Use this checklist before repeating the signup many times.

## 1. Check the complete recipient address

Compare the address submitted to the sender with the address currently shown in GPTMail. Check both sides of `@` and look for:

- a missing or repeated character;
- an accidental space;
- a different domain selected after the form was submitted;
- browser autofill replacing the temporary address with a saved personal address;
- an address copied from an older tab or session.

Email sent to a mistyped address cannot be moved into the intended inbox afterward.

## 2. Keep the original inbox open

If you generate another address immediately after submitting the form, the page may switch to the new inbox while the sender is still delivering to the old one. Open the original address directly or select it from recent addresses when available.

The Chrome extension can also retain the current address and show unread-message status without requiring the website tab to stay in front.

## 3. Wait for the sender

Verification email is asynchronous. Many messages arrive within seconds, but sender queues, regional providers, rate limits, and anti-abuse checks can create delays. Wait a few minutes before requesting another code.

Repeatedly clicking “send again” may make the situation worse. Some services invalidate earlier codes, suppress repeated messages, or temporarily throttle the destination.

## 4. Refresh the inbox once

GPTMail updates the inbox automatically where supported, but a manual refresh is a useful check after a connection interruption or a suspended mobile browser tab. Refresh once, then wait rather than polling continuously.

If the page was offline, restore the connection before assuming the message was not delivered.

## 5. Try another active domain

Some websites reject known disposable-email domains before sending any message. Others accept the form but silently suppress delivery later.

Choose **Auto** or another active domain and generate a new address. Submit the new address as a fresh attempt. Changing only the local part before `@` will not help when the sender blocks the entire domain.

A domain shown as unavailable, unsupported, or inactive should not be used for a new signup. GPTMail may replace an unsupported current address with a new supported one.

## 6. Confirm the website actually accepted the address

Look for an explicit success message after submitting the form. Client-side validation, CAPTCHA failure, an expired session, or an unrelated form error can prevent the request even when the email field looks valid.

If the website says the address is invalid or disposable email is not allowed, respect that policy. GPTMail cannot force another service to accept temporary addresses.

## 7. Check whether the sender is having trouble

The sending service may have its own outage or queue. Useful signs include:

- other transactional emails from the service are delayed;
- the resend button fails for multiple addresses;
- the service reports an incident;
- the confirmation page never states that a message was sent;
- the sender requires an additional step before email delivery.

When the sender never hands off the message, the receiving inbox has nothing to display.

## 8. Understand domain and MX health

A receiving domain needs valid MX records. DNS changes, an expired domain registration, or a record pointing to the wrong server can stop delivery. GPTMail monitors supported domains and may disable one whose routing no longer passes validation.

For a domain you own:

1. compare its MX record with the live target displayed by GPTMail;
2. remove accidental or conflicting records;
3. allow time for DNS propagation;
4. retry validation after several minutes;
5. confirm the domain registration and authoritative DNS are active.

For a public domain controlled by someone else, support cannot renew an expired domain or repair DNS without the owner's cooperation. Select another active domain instead.

## 9. Open the complete message when extraction is uncertain

A message may arrive even when GPTMail does not display a code in the summary. Verification formats vary, and a number in a footer, price, tracking URL, or date can look like a code.

Open the message and confirm:

- the sender and subject match the action you started;
- the message arrived after the request;
- the code format matches the website;
- the link points to the expected service.

Do not share verification codes or sign-in links with another person.

## 10. Use the right mailbox for important accounts

A temporary inbox is intentionally short-lived. GPTMail currently keeps email for 24 hours, and public inboxes are not confidential. Use a permanent mailbox you control for purchases, banking, identity, subscriptions you want to keep, account recovery, and long-term ownership.

## Quick decision guide

| Situation | Best next step |
| --- | --- |
| Address was mistyped | Submit the correct address again |
| Current inbox changed | Reopen the original address |
| Sender says “try later” | Wait before requesting another code |
| Website blocks disposable email | Use a permitted permanent address |
| Domain is unsupported | Generate a new address with Auto or another active domain |
| Your custom domain fails MX validation | Correct DNS, wait for propagation, and retry |
| Message arrived but no code is highlighted | Open and inspect the complete email |
| Account is valuable or long-term | Use a permanent private mailbox |

## Related resources

- [Open GPTMail](https://mail.chatgpt.org.uk/)
- [How temporary email works](how-temporary-email-works.md)
- [Custom domains and private inboxes](custom-domains-and-private-inboxes.md)
- [Temporary email vs email alias](temporary-email-vs-email-alias.md)
- [GPTMail help center](https://mail.chatgpt.org.uk/help)
