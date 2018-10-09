---
description: >-
  The email notification is required for the e-commerce website or App. In this
  section, we will tell you how to configure Send Mail feature on your server.
---

# Configure Email Notification

### Send Mail By PHP Mail\(\)

This method depends on PHP mail\(\) function, so you should make sure mail\(\) function is enabled on your server.  Generally speaking, this function is enabled by default on the most shared hosting, but if you use VPS, you may have to configure that by yourself. Please refer to guide: [https://blog.ashwinshenoy.com/php-send-mail-very-slow-9b0a4ace6672](https://blog.ashwinshenoy.com/php-send-mail-very-slow-9b0a4ace6672)

### Send Mail By SMTP Service \(Recommended\)

PHP mail\(\) method is not very reliable. We strongly recommended use the third-party Email service.  For example, [MailGun](https://www.mailgun.com/) is one of the best choices, 10,000 emails free every month.

#### 1. Create an account on MailGun

Just signup via [https://signup.mailgun.com/new/signup](https://signup.mailgun.com/new/signup) the credit card information is required, but you only need to pay out if more than 10,000 emails is sent in a month.

#### 2. Login and configure your domain DNS

Activate your account and login. Go to Domains page, and click "Add New Domain" button.

![](.gitbook/assets/image%20%2831%29.png)

Add a subdomain such as m.domain.com

![](.gitbook/assets/image%20%2823%29.png)

  
Then, follow the steps on this page to verify domain, you need to add some TXT, CNAME and MX record via your domain control panel.

![](.gitbook/assets/image%20%2832%29.png)

Once you make the above DNS changes **it can take 24-48hrs** for those changes to propagate. MailGun will email you to let you know once your domain is verified.

After that, back to the Domain page, you will see your domain status is active.

![](.gitbook/assets/image%20%2829%29.png)

Click your domain link to go to the setting page, you will get your SMTP certificate as below. Do not close this page.

![](.gitbook/assets/image%20%2815%29.png)

#### 3. Install Post SMTP Plugin

Login your WordPress backend, go to Plugins &gt; Add New page, search "**Post SMTP**" plugin and install &gt; activate this plugin.

![](.gitbook/assets/image%20%283%29.png)

Then, go to Post SMTP page, start the wizard.

![](.gitbook/assets/image%20%2817%29.png)

Enter the email address and name which you'd like to show as.

![](.gitbook/assets/image%20%2819%29.png)

Next, set the outgoing mail server hostname to **smtp.mailgun.org**

![](.gitbook/assets/image%20%2813%29.png)

Next, select **"SMTP - mailg**un.org:465"

![](.gitbook/assets/image%20%286%29.png)

Next, enter your SMTP username and password which you get from MailGun.

![](.gitbook/assets/image%20%2835%29.png)

Finished! Go back to Post SMTP page, click "Send a test email" link.

![](.gitbook/assets/image%20%2836%29.png)

Just add a valid email address and and start to test.

![](.gitbook/assets/image%20%2822%29.png)

Check this email inbox if it can receive the test mail.

That's it!

