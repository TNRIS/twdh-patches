# twdh-patches

* 0001-Resource-Views-on-Dataset-Pages.patch  
  * Updated read() function in ckan/views/dataset.py to allow for resource views to be shown on the dataset detail pages
  * 1 file changed, 31 insertions(+), 9 deletions(-)
    * ckan/views/dataset.py 
* 0002-Added-Support-for-HTML-Email.patch
  * Added Support for HTML Email
  * 6 new files
    * create mode 100644 ckan/templates/activity_streams/activity_stream_email_notifications.html
    * create mode 100644 ckan/templates/emails/base.html
    * create mode 100644 ckan/templates/emails/invite_user.html
    * create mode 100644 ckan/templates/emails/reset_password.html
    * create mode 100644 ckan/templates/emails/snippets/footer.html
    * create mode 100644 ckan/templates/emails/snippets/header.html
  * 8 files changed, 502 insertions(+), 10 deletions(-)
    * ckan/lib/email_notifications.py
    * ckan/lib/mailer.py
    * ckan/templates/activity_streams/activity_stream_email_notifications.html
    * ckan/templates/emails/base.html
    * ckan/templates/emails/invite_user.html
    * ckan/templates/emails/reset_password.html
    * ckan/templates/emails/snippets/footer.html
    * ckan/templates/emails/snippets/header.html
* 0003-ckanext-security-middleware.patch
  * This patch is based on the original [ckanext-security](https://github.com/data-govt-nz/ckanext-security) [patch file](https://github.com/data-govt-nz/ckanext-security/blob/master/ckanext-security.patch) but updated for CKAN 2.9.5
  * 2 files changed, 12 insertions(+), 2 deletions(-)
    * /ckan/config/middleware/flask_app.py
    * /ckan/config/middleware/pylons_app.py
* 0004-Welcome-Email-on-Invite-Acceptance.patch
  * When a user is invited to join CKAN, they receive an invitation email with a link to reset their password. When they reset the password and optionally modify their username, their account 'state' is changed from 'pending' to 'active' AND with this patch a welcome email also gets sent.
  * 1 file changed, 16 insertions(+)
    * /ckan/views/user.py
* 0005-Added-check-for-content-type-header-in-proxy_resource.patch
  * If a file requested from a remote server does not have 'content-type' set int he header, CKAN was crashing with a Flask stack trace. This patch catches this error and instead displays a 409 error to the user
  * 1 file changed, 9 insertions(+), 1 deletion(-)
    * ckanext/resourceproxy/blueprint.py 
* 0006-Added-cc-bcc-reply-to-to-mail_recipients.patch  
  * This patch adds the ability to cc and bcc, and override the default reply-to in the mail_recipients function in lib/mailer.py
  * 1 file changed, 10 insertions(+), 5 deletions(-)
    * ckan/lib/mailer.py
