---
title: "Configure email"
weight: 10
---

In this workshop you will use Email to send personalized email messages to your customers.

If you've closed the [Amazon Pinpoint Console](https://console.aws.amazon.com/pinpoint/), open it again. Navigate to your project, then **Settings**.

On the **Configure features** page, locate the Email channel. Click the **Configure**/**Manage** button to **Set up email**.

### Set up Email

Type an email address that you will use to send email. For example, you can use your personal email address, or your work email address. Click the **Verify** button and **keep this page open**.

![Set up email](/images/set-up-email.png)

Amazon Pinpoint sends a confirmation email to your address. Click the link in the message to verify your address.

![Confirm your email address](/images/validate-email.png)

Return to the **Set up email** page of the Amazon Pinpoint console. Your email address shows as verified. Click the **Save** button. 

Your email address is now verified. You are ready to send email messages.

### Sandbox environment

{{% notice note %}}
We use a sandbox environment to help protect our customers from fraud and abuse. In the sandbox environment you can send email only to addresses that you have verified.
{{% /notice %}}

To learn more about the sandbox environment, visit [Requesting Production Access for Email](https://docs.aws.amazon.com/pinpoint/latest/userguide/channels-email-setup-production-access.html) in the Amazon Pinpoint User Guide.

### Add additional email recipients

Since your project is in a sandbox environment, you need to validate all addresses to which you want to send emails. To add additional email addresses, open your project in the [Amazon Pinpoint Console](https://console.aws.amazon.com/pinpoint/). Navigate to **Settings** > **Email** > **Identity Details** > **Edit**. Now you can verify additional email identities.
