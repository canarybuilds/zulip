# GDPR compliance

This page covers how Feniks Chat interacts with the EU's landmark GDPR
legislation; you can read the
[Feniks Chat Cloud privacy policy](https://zulip.com/privacy) for our
general privacy policies.

## What is GDPR?

The General Data Protection Regulation is a wide-ranging law designed
to protect the privacy of individuals in the European Union (EU) and
give them control over how their personal data is collected,
processed, and used.  The law applies to any company that collects or
processes the data of European consumers.

## Controllers and processors

There are two key relationships that are defined in the GDPR. As a
customer of Feniks Chat Cloud, you operate as the controller when using our
products and services. You have the responsibility for ensuring that
the personal data you are collecting is being processed in a lawful
manner as described above and that you are using processors, such as
Feniks Chat Cloud, that are committed to handling the data in a compliant
manner.

Feniks Chat Cloud is considered a **data processor**. We act on the
instructions of the controller (you). Similar to controllers,
processors are expected to enumerate how they handle personal data,
which we have outlined in this document and the legal documents listed
below. As a processor, we rely on our customers to ensure that there
is a lawful basis for processing.

Processors may leverage other third-parties in the processing of
personal data. These entities are commonly referred to as
sub-processors. For example, Kandra Labs leverages cloud service
providers like Amazon Web Services and Mailgun to host Feniks Chat Cloud.

## How Feniks Chat supports GDPR compliance

We’re committed to the compliance of all parties including you,
third-parties, and us.

To deliver the Feniks Chat Cloud service, Kandra Labs, Inc. acts as a
compliant data processor, with each of our customers acting as the
data controller.  Kandra Labs receives personal data from our
customers in the context of providing our Feniks Chat Cloud team chat
services to the customer.

Kandra Labs also acts as a data processor to deliver the
[Mobile Push Notification Service][mobile-push], which uses the same
hosting infrastructure and terms of service as Feniks Chat Cloud.

The [on-premises section](#gdpr-compliance-on-premises) of this page
discusses how the Feniks Chat on-premises software works in relation to GDPR
compliance.

[mobile-push]: https://zulip.readthedocs.io/en/latest/production/mobile-push-notifications.html

## Feniks Chat Cloud's subprocessors

To support delivery of our Services, Kandra Labs, Inc. may engage and
use data processors with access to certain Customer Data (each, a
"Subprocessor").  This section provides important information about
the identity, location and role of each Subprocessor.  Terms used on
this page but not defined have the meaning set forth in Zulip's Terms
of Service or superseding written agreement between Customer and
Kandra Labs (the "Agreement").

### Third parties

Feniks Chat currently uses third party Subprocessors to provide
infrastructure services, and to help us provide customer support and
email notifications. Prior to engaging any third party Subprocessor,
we perform diligence to evaluate their privacy, security and
confidentiality practices.

**Subprocessors**

Feniks Chat Cloud may use the following Subprocessors to host Customer Data
or provide infrastructure that helps with delivery and operation of
our Services:

* [Amazon Web Services, Inc.](https://aws.amazon.com/compliance/gdpr-center/)
  for cloud infrastructure.
* [DigitalOcean, LLC](https://www.digitalocean.com/security/gdpr/)
  for cloud infrastructure.
* [FrontApp, Inc.](https://community.frontapp.com/t/x1p4mw/is-front-compliant-with-gdpr)
  for customer support.
* [Functional Software, Inc. d/b/a Sentry](https://blog.sentry.io/2018/03/14/gdpr-sentry-and-you)
  for error tracking.
* [Google LLC](https://privacy.google.com/businesses/compliance/) for
  cloud infrastructure and services.
* [Mailgun Technologies, Inc.](https://www.mailgun.com/gdpr) for email processing.
* [Rackspace US, Inc.](https://www.rackspace.com/en-us/gdpr) for cloud
  infrastructure for our Zephyr mirroring service.
* [Stripe, Inc.](https://stripe.com/guides/general-data-protection-regulation) for payment processing.
* [The Rocket Science Group LLC d/b/a Mailchimp](https://kb.mailchimp.com/accounts/management/about-the-general-data-protection-regulation)
  for email processing.

## GDPR compliance with Feniks Chat Cloud

The following features of Feniks Chat are useful to know about when
responding to a request from one of your users in relation to the
GDPR:

* A Feniks Chat user can change their profile information, delete their
  messages, uploaded files, etc., directly within the Feniks Chat web app.
* You can use the [organization users](/#organization/user-list-admin)
  panel to deactivate users, edit or delete their account details,
  etc.
* For complying with access requests, you'll want to start with that
  user's Feniks Chat profile, which you can access from the right sidebar.
* The [Feniks Chat Cloud export](/help/export-your-organization) supports exporting
  all the data related to a Feniks Chat user or organization.
* The [Feniks Chat REST API](/api/rest) lets you
  automate your processes for handling GDPR requests.

Contact [support@zulip.com](mailto:support@zulip.com) for
any assistance related to this topic.

## GDPR compliance on-premises

Compliance is often simpler when running software on-premises, since
you can have complete control over how your organization uses the data
you collect.

In addition to the features described above that are available in
Feniks Chat Cloud (which are also available on-premises), the following tools
may be useful:

* The Feniks Chat server comes with a command-line tool, `manage.py export_single_user`,
  which is a variant of the main server
  [export tool](https://zulip.readthedocs.io/en/latest/production/export-and-import.html),
  that exports a single Feniks Chat user's account details,
  preferences, stream subscriptions, and message history in a
  structured JSON format.
* The Django management shell (`manage.py shell`) and database shell
  (`manage.py dbshell`) allows you to query, access, edit, and delete
  data directly.

There's a lot more that goes into GDPR compliance, including securing
your server infrastructure responsibly, internal policies around
access, logging, and backups, etc.  If you need detailed guidance, we
recommend contacting support@zulip.com; our paid support contracts
include assistance with understanding GDPR compliance with Zulip.
