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
