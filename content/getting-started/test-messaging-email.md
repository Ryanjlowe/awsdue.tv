---
title: "Send an email message"
weight: 20
---

In the menu bar on the left hand side click on **Test Messaging** and select the **Email** channel.
![Test Messaging: Email Channel](/images/test-messaging-email-channel.png)

1. Select the **sender email address** that you have verified during the project setup.

1. Enter **your email address** that you verified for Destination type **Email address** as the recipient. This could be the same as your sender address, or additional email identities that you have verified. Amazon Pinpoint supports wildcard local parts. If you verified `fred@domain`, then `fred+foo@domain` will also work.

1. Select **Create a new message**. You will learn about the message templates feature in a couple of minutes.

1. Set the email **Subject**: `Sample Email`.

1. Copy/paste this code for the **Message** body:  
(Use the *Copy to clipboard* icon in the top right of the code window)  
```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0">
    <meta name="viewport" content="width=device-width" style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0">
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0">
    <title style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0">Amazon Pinpoint</title>
</head>
<body style="height:485px" topmargin="0" marginwidth="0" marginheight="0" leftmargin="0" contenteditable="true" bgcolor="#F2F3F3">
    <style>
        @media only screen and (max-width:600px) {
            a[class=btn] {
                display: block !important;
                margin-bottom: 10px !important;
                background-image: none !important;
                margin-right: 0 !important
            }

            div[class=column] {
                width: auto !important;
                float: none !important
            }

            table.social div[class=column] {
                width: auto !important
            }
        }
    </style>
    <p style="display:none;font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;font-size:14px;font-weight:400;line-height:1.6;margin:0;margin-bottom:10px;padding:0">This is a test message sent using Amazon Pinpoint.</p>
    <table class="head-wrap" style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0;width:100%" bgcolor="#000000">
        <tbody>
            <tr style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0">
                <td style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0"><img style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;height:35px;margin:0;max-width:100%;padding:12px;width:58px" src="https://docs.aws.amazon.com/assets/images/aws_logo_dark.png"></td>
                <td style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0; color:white; font-size: 44px;
        font-weight: bold;
        text-align: left;"> Pinpoint Workshop</td>
            </tr>
        </tbody>
    </table>
    <table class="body-wrap" style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0;width:100%">
        <tbody>
            <tr style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0">
                <td style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0"></td>
                <td class="container" style="clear:both!important;display:block!important;font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0 auto!important;max-width:602px!important;padding:0" bgcolor="#FFFFFF">
                    <div class="content" style="border-left:1px solid #c9cfd0;border-right:1px solid #c9cfd0;border-top:1px solid #c9cfd0;display:block;font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:1rem auto 0 auto;max-width:600px;padding:10px 10px 0px 10px">
                  
                        <h1 style="color:#000;font-family:HelveticaNeue-Light,'Helvetica Neue Light','Helvetica Neue',Helvetica,Arial,'Lucida Grande',sans-serif;font-size:44px;font-weight:600;margin:0;margin-bottom:15px;padding:0">Demo Test Message</h1>
                        

                    </div>
                    <div class="column-wrap" style="border-bottom:1px solid #c9cfd0;border-left:1px solid #c9cfd0;border-right:1px solid #c9cfd0;font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0 auto;max-width:600px!important;padding:0!important">
                        <div class="column" style="float:left;font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0;width:600px">
                            <table style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0;width:100%">
                                <tbody>
                                    <tr style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0">
                                        <td style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:15px">
                                            <p>Thanks for working through the <a href="https://www.pinpoint-workshop.com/">Amazon Pinpoint Workshop</a></p>
                                            <p>This email was send in the getting started section.</p>
                                        </td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                        <div class="clear" style="clear:both;display:block;font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0"></div>
                    </div>
                </td>
                <td style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0"></td>
            </tr>
        </tbody>
    </table>
    <table class="footer-wrap" style="clear:both!important;font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0;width:100%">
        <tbody>
            <tr style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0">
                <td style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0"></td>
                <td class="container" style="clear:both!important;display:block!important;font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0 auto!important;max-width:602px!important;padding:0">
                    <div class="content-footer" style="display:block;font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0 auto;max-width:600px;padding:15px">
                        <table style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0">
                            <tbody>
                                <tr style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0">
                                    <td style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0" align="center">
                                        <p style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;font-size:x-small;font-weight:400;line-height:1.6;margin:0;margin-bottom:10px;padding:0">This message was sent using <a href="https://aws.amazon.com/pinpoint/" style="color:#2BA6CB;font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0;text-decoration:none">Amazon Pinpoint</a>.</p>
                                        <hr style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;margin-bottom:10px;padding:0">
                                        <p style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;font-size:x-small;font-weight:400;line-height:1.6;margin:0;margin-bottom:10px;padding:0">Amazon Web Services, Inc. is a subsidiary of Amazon.com, Inc. Amazon.com is a registered trademark of Amazon.com. This message was produced and distributed by Amazon Web Services, Inc. and its affiliates, 410 Terry Ave. North, Seattle, WA 98109.</p>
                                        <p style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;font-size:x-small;font-weight:400;line-height:1.6;margin:0;margin-bottom:10px;padding:0">&#xA9; 2019, Amazon Web Services, Inc. or its affiliates. All rights reserved. Read our <a href="https://aws.amazon.com/privacy" style="color:#2BA6CB;font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0;text-decoration:none">Privacy Policy</a>.</p>
                                        <p style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;font-size:x-small;font-weight:400;line-height:1.6;margin:0;margin-bottom:10px;padding:0"><a ses:tags="unsubscribeLinkTag:click;" style="color:#2BA6CB;font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0;text-decoration:none" href="http://www.example.com/unsubscribe">Click here to unsubscribe.</a></p>
                                    </td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </td>
                <td style="font-family:'Helvetica Neue',Helvetica,Helvetica,Arial,sans-serif;margin:0;padding:0"></td>
            </tr>
        </tbody>
    </table>
</body>
</html>
```

Be sure to **paste** the copied code into your **Message** body. 
Optionally, preview the message before you send it.

![Create a test email message](/images/test-messaging-email.png)

Click the **Send message** button and check your inbox.

You have received your first email from Amazon Pinpoint.
