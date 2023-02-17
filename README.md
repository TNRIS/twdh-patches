# twdh-patches

* Note that _main_ currently consists of patches against CKAN 2.9.8
* We will not create a tag for _v2.9.8_ until we do another upgrade, in case there are changes to existing patches or new patches are added applying to v2.9.8
* If you need patches against CKAN 2.9.5, be sure to pull using the _v2.9.5_ tag.

* 0001-Resource-Views-on-Dataset-Pages.patch  
  * Updated read() function in ckan/views/dataset.py to allow for resource views to be shown on the dataset detail pages
* 0002-Added-Support-for-HTML-Email.patch
  * Added Support for HTML Email
* 0003-ckanext-security-middleware.patch
  * This patch is based on the original [ckanext-security](https://github.com/data-govt-nz/ckanext-security) [patch file](https://github.com/data-govt-nz/ckanext-security/blob/master/ckanext-security.patch) but updated for CKAN 2.9.5
* 0004-Welcome-Email-on-Invite-Acceptance.patch
  * When a user is invited to join CKAN, they receive an invitation email with a link to reset their password. When they reset the password and optionally modify their username, their account 'state' is changed from 'pending' to 'active' AND with this patch a welcome email also gets sent.
* 0005-Added-check-for-content-type-header-in-proxy_resource.patch
  * If a file requested from a remote server does not have 'content-type' set int he header, CKAN was crashing with a Flask stack trace. This patch catches this error and instead displays a 409 error to the user
* 0006-Added-cc-bcc-reply-to-to-mail_recipients.patch  
  * This patch adds the ability to cc and bcc, and override the default reply-to in the mail_recipients function in lib/mailer.py
