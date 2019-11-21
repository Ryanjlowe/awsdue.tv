+++
title = "Create a Pinpoint Project"
chapter = false
weight = 20
+++

## to do:
- [ ] fix region in urls
- [ ] sandbox info
- [ ] should we educate on endpoint limits
- [ ] Test SMS image

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
