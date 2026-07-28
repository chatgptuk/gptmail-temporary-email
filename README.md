<p align="center">
  <a href="https://mail.chatgpt.org.uk/">
    <img src="https://mail.chatgpt.org.uk/logo.svg" width="88" height="88" alt="GPTMail temporary email logo">
  </a>
</p>

<h1 align="center">GPTMail — Free Temporary Email</h1>

<p align="center">
  Create a disposable inbox in seconds, receive verification codes, keep spam away from your personal email, and use custom domains when you need more control.
</p>

<p align="center">
  <a href="https://mail.chatgpt.org.uk/"><strong>Open GPTMail</strong></a> ·
  <a href="https://chromewebstore.google.com/detail/eplebonhkjiahfnoaiifngokamaipeoo">Chrome extension</a> ·
  <a href="docs/README.md">Guides</a> ·
  <a href="https://mail.chatgpt.org.uk/help">Help</a> ·
  <a href="https://mail.chatgpt.org.uk/api">Developer API</a>
</p>

<p align="center">
  <a href="README.zh-CN.md">简体中文</a> ·
  <a href="README.id.md">Bahasa Indonesia</a> ·
  <strong>English</strong>
</p>

[![GPTMail free temporary email interface](https://mail.chatgpt.org.uk/og.png)](https://mail.chatgpt.org.uk/)

## A temporary inbox without the usual friction

GPTMail is a free temporary email service for short-lived signups, verification emails, software testing, and situations where sharing a permanent address would create unnecessary spam. Open the website and an address is ready to use; no account registration is required for a public inbox.

A temporary email is not a replacement for a permanent mailbox. It is a focused tool for messages that only need to exist briefly. GPTMail keeps email for **24 hours**, giving you time to receive a code or confirmation link without turning a one-time interaction into years of marketing email.

## What GPTMail offers

| Feature | What it is useful for |
| --- | --- |
| Instant disposable address | Start receiving email without creating an account |
| Verification-code extraction | Find common one-time codes and confirmation links faster |
| Multiple active domains | Switch domains when a website does not accept the first address |
| Custom prefix | Create a recognizable address for a test or short workflow |
| Public and private domain inboxes | Use a simple public inbox or a password-protected private-domain inbox |
| Bring your own domain | Point a domain you control to GPTMail for more predictable addresses |
| Chrome extension | Create addresses, check messages, and fill email fields from the browser |
| Developer API | Automate inbox creation and email checks in QA and test workflows |
| Telegram monitoring | Receive new-message alerts for an active inbox |
| Responsive interface | Use the inbox on desktop or mobile without installing an app |

## How to use a free temporary email

1. Visit **[mail.chatgpt.org.uk](https://mail.chatgpt.org.uk/)**.
2. Use the address already generated for you, or select **Random** for another address.
3. Paste that address into the signup, trial, download, or test form.
4. Return to GPTMail and wait for the message to appear in the inbox.
5. Open the email to read its verification code or confirmation link.

If a service rejects one temporary-email domain, choose another active domain from the selector and generate a new address. Domain availability can change because each receiving domain depends on valid DNS and MX configuration.

## Chrome extension

The **[GPTMail Chrome extension](https://chromewebstore.google.com/detail/eplebonhkjiahfnoaiifngokamaipeoo)** keeps the temporary inbox close to the page where you need it. It can:

- create and switch temporary addresses;
- show unread messages from the toolbar or side panel;
- notify you when new email arrives;
- suggest the active address in email fields after you enable that optional feature;
- keep each browser installation independently authorized without embedding a shared API key.

The extension is useful for repeated testing and signup workflows, while the website remains fully usable on its own.

## Public inboxes, private inboxes, and custom domains

A **public inbox** is convenient but not confidential. Anyone who knows the complete email address may be able to open it. Never use a public temporary inbox for banking, identity documents, medical information, password recovery, long-term accounts, or private conversations.

For more control, GPTMail supports domains that you own:

- **Public custom domain:** addresses on the domain work like other public GPTMail inboxes.
- **Private custom domain:** inbox access is protected by the private password configured for that domain.
- **Cloudflare-assisted DNS setup:** domain owners can authorize a narrowly scoped flow to add the required MX record instead of entering it manually.

Read the practical guide: **[Custom domains and private inboxes](docs/custom-domains-and-private-inboxes.md)**.

## Temporary email for developers and QA teams

Disposable inboxes are useful in automated tests where a real message must be received:

- account-registration and email-verification tests;
- passwordless sign-in and magic-link testing;
- staging-environment notifications;
- end-to-end tests that need a unique address;
- deliverability checks during product development;
- disposable test data that should not reach employee inboxes.

GPTMail provides a browser interface and an HTTP API. Use API keys in request headers, keep credentials out of URLs and logs, and design tests to tolerate normal email-delivery delays. See **[Testing and API workflows](docs/testing-and-api-workflows.md)** and the live **[API documentation](https://mail.chatgpt.org.uk/api)**.

## Frequently asked questions

### What is a temporary email?

A temporary email is a short-lived address used to receive messages without exposing a permanent personal or work inbox. It is commonly called disposable email, temp mail, throwaway email, or a temporary inbox.

### Can GPTMail receive verification codes?

Yes. GPTMail receives normal email sent to supported domains and can highlight many common verification codes and confirmation links. Extraction is a convenience feature; always check the full message when accuracy matters.

### Do I need to register?

No registration is required to use a public temporary inbox. Private-domain features require the password chosen by the domain owner.

### How long are messages kept?

GPTMail currently retains email for 24 hours. A message may disappear earlier if the user deletes it or clears the inbox.

### Is a public temporary inbox private?

No. Treat every public inbox as discoverable by anyone who knows the address. Use it only for low-risk, short-lived messages.

### Does GPTMail create Gmail or other permanent accounts?

No. GPTMail provides temporary inboxes on supported domains; it does not create Gmail, Outlook, or other third-party accounts.

### Can I use my own domain?

Yes. GPTMail can validate a domain whose MX record points to the required receiving target. Public and password-protected private modes are available.

## Responsible use

Use GPTMail only where temporary addresses are permitted. Do not use it for fraud, harassment, unsolicited messaging, bypassing platform safeguards, or receiving sensitive information. A website may block disposable addresses, and GPTMail cannot guarantee that every third-party service will accept every domain.

## Learn more

- **[Documentation hub](docs/README.md)**
- **[How temporary email works](docs/how-temporary-email-works.md)**
- **[Verification email not received?](docs/verification-email-not-received.md)**
- **[Temporary email vs email alias](docs/temporary-email-vs-email-alias.md)**
- **[Custom domains and private inboxes](docs/custom-domains-and-private-inboxes.md)**
- **[Testing and API workflows](docs/testing-and-api-workflows.md)**
- **[GPTMail help center](https://mail.chatgpt.org.uk/help)**
- **[Support](SUPPORT.md)** and **[security policy](SECURITY.md)**
- **[Contributing to the documentation](CONTRIBUTING.md)**
- **[Terms and privacy](https://mail.chatgpt.org.uk/terms)**
- **[Product updates and guides](https://mail.chatgpt.org.uk/blog)**

---

GPTMail is not affiliated with OpenAI, ChatGPT, Google, Microsoft, Telegram, or any other third-party service mentioned in this documentation. Product names belong to their respective owners.