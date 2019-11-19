+++
title = "Pinpoint Setup"
chapter = false
weight = 20
+++

## to do:
- [ ] fix region in urls
- [ ] sandbox info
- [ ] should we educate on endpoint limits
- [ ] Test SMS image

## Step 1: Create Pinpoint Project

**This workshop has been tested in {{INSERT REGION HERE}}**

### Initial Configuration

1. First head to Amazon Pinpoint in the [AWS Console](https://us-west-2.console.aws.amazon.com/pinpoint/home?region=us-west-2#/apps). Enter a project name of `pinpointWorkshop` and click on the 'Create a project' button ![pinpointConsole](/images/pinpoint-get-started.png) 
2. For this workshop we will cover Email and SMS And voice, so first of all click on `Configure` underneath  Email.![emailconfig](/images/pinpoint-created-project.png) 
3. We have to validate that you own the email address to stop people being able to send emails with incorrect emails adresses. This lab requires you to validate your email address (and we will do more later on). Enter your email address and click verify. You will be instantly emailed a link which you need to click on to verify you own the account.![emailconfig](/images/validate-email.png)
4. Click Save.
5. If you want to be able to send emails (while in sandbox mode [insert url]) to other accounts you will have to add these as well. You can do this by going to `Settings -> Email -> Identity Details -> Edit` and then adding and verifying a new email address.
6. There are also limits you may want to enable...
7. You are also able to send SNS via Pinpoint but as with Emails, you need to enable this first. To do this go to  `Settings -> SMS and Voice -> Edit` and enable the SMS channel for this project.

You Pinpoint project is now ready to send messages.

## Step 2: Sending some test messages


In the menu bar on the left hand side click on `Test Messaging`.

### Test Email

1. Click on `Email`.
2. The sender email address should already be configured following the setup in Lab 1.
3. Enter the same email address in the destination as the sender (as we know this address is verified)
4. Create a simple message and enter a subject line then click `Send message` - now check your inbox as you should have mail!![pinpointConsole](/images/message-template.png)

### Test SMS

1. Click on `SMS`
2. Enter your Phone numbers
3. Fill in a message body
4. Click send message.


