+++
title = "Create a message template"
chapter = false
weight = 80
+++

You can use **message templates** to design consistent messages and reuse content more effectively, even between projects. You can define message templates for email messages, push notifications, SMS messages, and voice messages.

As your last step in this chapter, you will learn how to create your first message template to **Welcome your users**. You will re-use these steps in the next chapter, where you need to create several more templates.

1. Navigate to the [Amazon Pinpoint Console](https://console.aws.amazon.com/pinpoint/), then **Message templates**.

1. Click **Create a template**.
![Create a template](/images/create-a-message-template.png)

1. Choose **Email** for the channel.
![Message template channel](/images/message-template-channel.png)

1. Use a descriptive **Name** for your new template. This will help you identify the template later when you need to choose from a list of templates. The **Description** is optional.  
**Name**: *WelcomeEmail*.  
![Message Template Details](/images/message-template-details.png)

1. Since this is an email template, configure the email **Subject** and **Message** body.  
**Subject**: *Welcome to your workshop: Multichannel customer engagement using Amazon Pinpoint*  
![Message Template Email Subject](/images/message-template-email-subject.png)

1. Open, select all, and copy the HTML code from the [Welcome Email](/email-templates/welcome-email.txt)  
... and paste it into the **Message** body of your template.
![Message Template Email Message](/images/message-template-email-message.png)

1. Click **Create** to save your new message template.

### Adding Personalized Content to Message Templates

You can personalize the subject and body of the template. To do this, add message variables that refer to specific attributes that you or Amazon Pinpoint created for the project, such as an attribute that stores a user's first name.

Your workshop uses personalized message templates. You can see the dynamic attributes in action inside the `{{` and `}}` handlebars.


{{% notice tip %}}
To learn more about message templates, visit [Amazon Pinpoint Message Templates](https://docs.aws.amazon.com/pinpoint/latest/userguide/messages-templates.html) in the Amazon Pinpoint User Guide.

{{% /notice %}}
