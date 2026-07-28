# How Temporary Email Works

A temporary email address is a short-lived receiving address designed for messages that do not need a permanent home. It is often described as disposable email, temp mail, throwaway email, or a temporary inbox.

The basic idea is simple: instead of giving a website your personal or work address, you use an address created for one short interaction. The website sends its verification code, confirmation link, receipt, or test message to that address. You read the message, complete the task, and leave your permanent inbox out of the exchange.

## The normal message flow

1. A temporary-email service provides an address on one of its active domains.
2. You enter that address on a third-party website or in a test application.
3. The sender looks up the domain's mail-exchange (MX) records.
4. The email is delivered to the receiving service.
5. The message appears in the temporary inbox associated with the full address.
6. Retention rules remove the message after a limited period.

GPTMail currently retains email for 24 hours. This is long enough for delayed verification messages while still keeping the inbox intentionally temporary.

## Why people use a temporary inbox

### Reduce marketing email

A one-time download or trial can lead to years of newsletters. A disposable address keeps that marketing stream separate from a mailbox used for work, family, and account recovery.

### Receive verification codes

Many services confirm an address by sending a short numeric code or a link. GPTMail can highlight common verification codes and links, while still allowing the complete message to be opened for context.

### Test real email delivery

Developers and QA teams often need a unique address for every test run. A temporary inbox can receive the same message a real user would receive without filling employee accounts with test data.

### Limit unnecessary disclosure

An email address can become a durable identifier shared across data brokers and marketing systems. Using a separate temporary address for a low-risk interaction limits how widely a primary address is distributed.

## What a temporary email cannot guarantee

Temporary email is useful, but it is not anonymous by itself and it is not a secure vault.

- A public inbox may be accessible to anyone who knows the full address.
- The sender still sees the temporary address and other normal connection data from its own website.
- A third-party website may reject disposable-email domains.
- Delivery can be delayed by the sender, DNS, spam filtering, or network conditions.
- Automated extraction may not identify every verification code or link correctly.
- Messages disappear when the retention period ends or when the inbox is cleared.

For those reasons, a temporary inbox should not be used for banking, government services, identity records, medical information, cryptocurrency accounts, password recovery, or any account you expect to keep.

## Public inbox or private inbox?

A public inbox provides the fastest experience: enter the complete address and view the messages. That convenience means the address itself acts as the lookup key, so secrecy depends on nobody else knowing or guessing it.

A private-domain inbox adds an access password controlled by the domain owner. It is more appropriate when a team or individual wants temporary retention while keeping inbox access restricted. The email is still temporary, and the password should not be reused elsewhere.

## Domain availability and MX records

Email reaches a service because the receiving domain publishes MX records. If those records expire, change, or point somewhere else, the domain may stop receiving through GPTMail. This is why the active-domain list can change over time.

When using your own domain, follow the MX target displayed by GPTMail rather than copying a value from an old guide. DNS changes also need time to propagate, so a newly added record may not validate immediately.

## A practical rule

Use temporary email for information that is **short-lived and low risk**. Use a permanent mailbox you control for anything involving money, identity, recovery, long-term ownership, or important personal communication.

## Try GPTMail

- [Create a free temporary email](https://mail.chatgpt.org.uk/)
- [Install the GPTMail Chrome extension](https://chromewebstore.google.com/detail/eplebonhkjiahfnoaiifngokamaipeoo)
- [Read the help center](https://mail.chatgpt.org.uk/help)
- [Review terms and privacy](https://mail.chatgpt.org.uk/terms)
