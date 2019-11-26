+++
title = "Create a campaign"
chapter = false
weight = 60
+++

Engage your audience by creating a messaging campaign. A campaign sends tailored messages on a schedule that you define. You can create campaigns that send push notifications, email, SMS text messages, and voice messages.

To experiment with alternative campaign strategies, set up your campaign as an A/B test, and analyze the results with Amazon Pinpoint analytics.

Let's go through the steps needed to see a campaign in action.

## Create a Campaign

1. Navigate to your project in the [Amazon Pinpoint Console](https://console.aws.amazon.com/pinpoint/), then **Campaigns**.

1. Choose **Create a campaign**.
![Create a campaign](/images/create-a-campaign.png)

1. Configure the campaign name, type, and channel. Click **Next**.
![Campaign details](/images/campaign-details.png)

1. Select **Use an existing segment** and select the segment you imported earlier. Click **Next**.

1. In the **Create your message** step you define the sender address, subject line, and message body for an email campaign. This step will look different depending on the channel you configured for this campaign. Click **Next**.

1. Now you **Choose when to send the campaign**. Dynamic segments can be triggered by events. Since your workshop segment is imported and thus static, you configure a time and reccurrence for the campaign, not when an event occurs. Choose **Immediately** to deliver the message when you launch the campaign.
![Send campaign immediately](/images/send-campaign-immediately.png)
To prevent users from receiving your messages at inconvenient times, you can also configure your campaigns so that they don't send messages during specific quiet hours. Click **Next**.
![Campaign quiet times](/images/campaign-quiet-times.png)

1. Review your campaign settings. Click **Launch campaign**.

You have defined your imported user segment, created your message, and launched the campaign. You have engaged your users based on conditions that you have defined.

When you define campaigns for dynamic segments, you can respond to your users actions as soon as your project receives events. For example, it can invite users back to your app who haven’t run it recently, or send a campaign when a user creates a new account.

<!-- 
To learn more about campaigns, visit [Amazon Pinpoint Campaigns](https://docs.aws.amazon.com/pinpoint/latest/userguide/campaigns.html) in the Amazon Pinpoint User Guide.
-->
