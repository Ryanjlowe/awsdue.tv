+++
title = "Create a segment"
chapter = false
weight = 50
+++

Reach the right audience for your messages by defining audience segments. A segment designates which users receive the messages that are sent from a campaign or journey. You can define dynamic segments based on data that's reported by your application, such as operating system or mobile device type. You can also import static segments that you define outside of Amazon Pinpoint.

In the next step you'll import segment that contains several users with user attributes.

### Prepare your segment

In this workshop you will start with a list of users in a CSV file. This is useful in situations where you define user segments outside of Amazon Pinpoint and want to engage your users with Amazon Pinpoint campaigns.  
In a couple of minutes, you'll send customized messages to these users.

To get started with your segment import you need to define the details of your users and endpoints. This can be an email address, or another destination that can receive messages, such as mobile device identifier, or mobile phone number. Let's keep it simple and go with email.

1. Download the [sample CSV file](/csv/activeSegment.csv) and open it in a text editor on your computer.

1. Add/edit a couple of users using the wildcard local parts notation you saw when you sent a test message.  
Edit the `Address` column in the CSV file to reflect email addresses you verified in the [Configure Email section ](../configure-email/).  
Example: If you verified `fred@domain`, then `fred+foo@domain`, `fred+bar@domain`, etc. will also work.  
```csv
ChannelType,Address,User.UserId,User.UserAttributes.FirstName,User.UserAttributes.LastName,User.UserAttributes.age,User.UserAttributes.isActive
EMAIL,Raymond+pinpoint1@emaildomain.com,userid1,Raymond,Phillips,35,TRUE
EMAIL,Sue+pinpoint2@emaildomain.com,userid2,Sue,Sherman,31,FALSE
EMAIL,Mark+pinpoint3@emaildomain.com,userid3,Mark,Price,28,
```
Please ensure that you have at least two verified email addresses for userid1 and userid2.  
Finally, double check to make sure that all email addresses you entered are valid. 

1. Save the file and remember its location on your computer. You will need this in the next step.

### Import a segment

To import a segment, you define the endpoints or user IDs that belong to your segment in a comma-separated values (CSV) or JSON file. Then you import the file into Amazon Pinpoint to create the segment.

Since you're uploading a single file under 1GB, you can upload the file directly to the console.

1. Navigate to your project in the [Amazon Pinpoint Console](https://console.aws.amazon.com/pinpoint/), then **Segments**.

1. Choose **Create a segment**.
![Create a segment](/images/create_a_segment.png)

1. Choose **Import a segment**.
![Import a segment](/images/import-a-segment.png)

1. Choose **Upload files from your computer** and drop the CSV file you just saved in the last step into the *Drop files here* area, or click **Choose files** and browse to your CSV import file.

1. Provide a descriptive name for your segment. Click **Create segment** to complete the import.
![Name your segment and complete the import](/images/complete-the-import.png)

1. After a couple of seconds your segment will be imported. Click on the segment name to view its details.

You have imported users and endpoints into your project. Your project is set up to engage with these users based on rules and conditions that you will define next.

<!-- 
To learn more about segments, visit [Amazon Pinpoint Segments](https://docs.aws.amazon.com/pinpoint/latest/userguide/segments.html) in the Amazon Pinpoint User Guide.
-->
