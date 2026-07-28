# Custom Domains and Private Inboxes

A shared temporary-email domain is ideal when you need an address immediately. A custom domain is better when you want a recognizable suffix, more predictable addresses, or password-protected access for short-lived messages.

GPTMail supports both public and private custom-domain modes. In each case, the domain owner must control the domain's DNS and point its mail exchange to the target currently shown by GPTMail.

## Public custom domains

A public custom domain joins the public domain pool. Addresses on that domain work like other public GPTMail inboxes: anyone who knows a complete address may be able to open its inbox.

This mode can be useful for:

- a test domain shared by a development team;
- disposable addresses used in public demonstrations;
- QA environments where messages contain no sensitive information;
- a recognizable domain suffix without account management.

Do not use public mode for confidential messages. Owning the domain does not make individual public inboxes private.

## Private custom domains

Private mode adds a domain-level access password. Before an inbox on that domain can be opened, the visitor must supply the password configured by the domain owner.

Private domains are useful when you want:

- temporary retention with controlled inbox access;
- catch-all-style addresses for internal testing;
- a domain reserved for one person or team;
- fewer accidental views of test messages.

The password protects access through GPTMail, but it does not turn temporary email into permanent encrypted storage. Choose a unique password, do not reuse an important credential, and keep sensitive or long-term accounts in a permanent mailbox.

## MX records explained

An MX record tells sending mail servers where a domain receives email. GPTMail accepts a custom domain only after checking that its MX record points to the required receiving target.

The correct target is shown on the GPTMail website. Use that live value because infrastructure and domain settings can change. A typical DNS entry contains:

- **Type:** MX
- **Name:** `@` or the root domain, depending on the DNS provider
- **Target:** the value currently displayed by GPTMail
- **Priority:** the value recommended by the setup flow

A lower numeric priority is normally preferred by mail senders. Remove conflicting MX records unless you intentionally operate multiple receiving systems and understand the delivery consequences.

## DNS propagation

DNS changes are not always visible everywhere immediately. If validation fails just after adding the record:

1. confirm that the record was saved on the authoritative DNS provider;
2. check for typographical errors or a trailing domain added twice;
3. make sure the record is attached to the intended root domain;
4. wait several minutes and retry;
5. check whether an old MX record is still cached or has a long TTL.

Repeated validation failures do not necessarily mean the domain is broken. They often indicate that the new record has not propagated to the resolver being queried.

## Cloudflare-assisted setup

For domains using Cloudflare DNS, GPTMail can offer an authorization flow that adds the required MX record. The flow is intended to reduce configuration errors for users who are unfamiliar with DNS.

Review the authorization screen before approving it. GPTMail's setup is designed around the record required for mail delivery; it is not a request to transfer ownership of the domain. Existing DNS records should still be reviewed carefully before making any mail-routing change.

## Root domains and subdomains

A custom email domain may be a root domain you control or, where supported by the setup flow, a subdomain under a root domain you control. The important requirement is genuine DNS control. A free or shared subdomain supplied by an unrelated hosting platform may not provide the authority or reliability needed for mail routing.

## Ongoing validation

MX configuration can change after a domain is added. GPTMail periodically checks domain health and may disable a domain whose mail routing no longer points to the required receiving target. This protects users from generating addresses that cannot receive mail.

Domain registration also matters. If a domain expires or its DNS service is suspended, GPTMail cannot restore it. The domain owner is responsible for renewal and DNS availability.

## Add your domain

Open **[GPTMail](https://mail.chatgpt.org.uk/)** and find **Bring Your Own Domain**. Choose public or private mode, follow the MX instructions, and retry validation after DNS propagation if necessary.

Related reading:

- [How temporary email works](how-temporary-email-works.md)
- [Testing and API workflows](testing-and-api-workflows.md)
- [GPTMail help center](https://mail.chatgpt.org.uk/help)
