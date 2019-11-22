---
title: "Configure Email"
date: 2019-11-22T17:54:28+01:00
draft: true
chapter: false
weight: 10
---

In this workshop you will use Email to send personalized email messages to your customers, and SMS and voice to send SMS text messages from shared or reserved phone numbers.

On the Configure features page, under Messaging channels and response metrics, click the {{% button %}}Configure{{% /button %}} button next to Email.

![Enter your email address](/images/enter-an-email-address.png)

Type an email address that you want to use to send email. For example, you can use your personal email address, or your work email address. Click {{% button %}}Verify{{% /button %}} and keep this page open.

Amazon Pinpoint sends a confirmation email to your address. Click the link in the message to verify your address.

![Confirm your email address](/images/validate-email.png)

Return to the Set up email page of the Amazon Pinpoint console in your browser. Click {{% button %}}Save{{% /button %}}. 

Your email address is now verified and you are ready to send messages.

### Sandbox

{{% notice note %}}
We use a sandbox environment to help protect our customers from fraud and abuse. In the sandbox environment you can send email only to addresses that you have verified.
{{% /notice %}}

To learn more about the sandbox environment, visit [Requesting Production Access for Email](https://docs.aws.amazon.com/pinpoint/latest/userguide/channels-email-setup-production-access.html) in the Amazon Pinpoint User Guide.


## TODO:
5. If you want to be able to send emails (while in sandbox mode [insert url]) to other accounts you will have to add these as well. You can do this by going to `Settings -> Email -> Identity Details -> Edit` and then adding and verifying a new email address.
6. There are also limits you may want to enable...
7. You are also able to send SNS via Pinpoint but as with Emails, you need to enable this first. To do this go to  `Settings -> SMS and Voice -> Edit` and enable the SMS channel for this project.

