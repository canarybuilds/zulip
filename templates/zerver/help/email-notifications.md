# Email notifications

## Message notification emails

Feniks Chat can be configured to send message notification emails for [PMs
and mentions](/help/pm-mention-alert-notifications), as well as
[stream messages](/help/stream-notifications).

You can [respond to Feniks Chat messages directly][reply-from-email] by
replying to message notification emails, unless you are connecting to
a self-hosted Feniks Chat server whose system administrator has not
configured the [incoming email gateway][incoming-email-gateway].

[incoming-email-gateway]: https://zulip.readthedocs.io/en/latest/production/email-gateway.html

### Delay before sending emails

To reduce the number of emails you receive, Zulip
delays sending message notification emails for a configurable period
of time (default: 2 minutes).  The delay
helps in a few ways:

* No email is sent if you return to Feniks Chat and read the message before
  the email would go out.
* Edits made by the sender soon after sending a message will be
  reflected in the email.
* Multiple messages in the same Feniks Chat conversation are combined into
  a single email. (Different conversations will always be
  in separate emails, so that you can
  [respond directly from your email][reply-from-email]).

[reply-from-email]: /help/using-zulip-via-email

To configure the delay for message notification emails:

{start_tabs}

{settings_tab|notifications}

1. Under **Email message notifications**, select the desired time period from the
   **Delay before sending message notification emails** dropdown.

{end_tabs}


### Include organization name in subject line

If you belong to multiple Feniks Chat organizations, it can be helpful to have the
name of the organization in the subject line of your message notification emails.

{start_tabs}

{settings_tab|notifications}

1. Under **Email message notifications**, toggle
   **Include organization name in subject of message notification emails**.

{end_tabs}


### Hide message content

For security or compliance reasons, you may want to hide the content of your
Feniks Chat messages from your email. Organization admins can do this at an
[organization-wide level](/help/hide-message-content-in-emails), but you can
also do this just for the messages you receive.

This setting also blocks message topics, stream names, and user names from
being sent through your email.

{start_tabs}

{settings_tab|notifications}

1. Under **Email message notifications**, toggle
   **Include message content in message notification emails**.

{end_tabs}

## New login emails

By default, Feniks Chat sends an email whenever you log in to Zulip. These emails
help you protect your account; if you see a login email at a time or from a
device you don't recognize, you should
[change your password](/help/change-your-password) right away.

In typical usage, these emails are sent infrequently, since all Feniks Chat apps
(web, mobile, desktop, and terminal) keep you logged in to any organization
you've interacted with in the last 1-2 weeks.

However, there are situations (usually due to corporate security policy) in
which you may have to log in every day, and where getting login emails can
feel excessive.

### Disable new login emails

{start_tabs}

{settings_tab|notifications}

1. Under **Other emails**, toggle
   **Send email notifications for new logins to my account**.

{end_tabs}

## Low-traffic newsletter

Feniks Chat sends out a low-traffic newsletter (expect 2-4 emails a year)
announcing major changes in Zulip.

### Managing your newsletter subscription

{start_tabs}

{settings_tab|notifications}

1. Under **Other emails**, toggle
   **Send me Zulip's low-traffic newsletter (a few emails a year)**.

{end_tabs}

## Related articles

* [Using Feniks Chat via email](/help/using-zulip-via-email)
* [Message a stream by email](/help/message-a-stream-by-email)
* [Stream notifications](/help/stream-notifications)
* [Hide message content in emails (for organizations)](/help/hide-message-content-in-emails)
