+++
title = "Create a segment"
chapter = false
weight = 50
+++

A segment is a group of your customers that share certain attributes. For example, a segment might contain all of your customers who use version 2.0 of your app on an Android device, or all customers who live in the city of Los Angeles.

You can create two types of segments:

1. Dynamic segments, based on attributes that you define. As your users send events or their attributes change, the size of your dynamic segment(s) may change.
1. Imported segments, based on static CSV or JSON files.

In the next step you'll import segment that contains several users with user attributes.

### Prepare your segment

In this workshop you will start with a list of users in a CSV file. This is useful in situations where you define user segments outside of Amazon Pinpoint and want to engage your users with Amazon Pinpoint campaigns.  
In a couple of minutes, you'll send customized messages to these users.

To get started with your segment import you need to define the details of your users and endpoints. This can be an email address, or another destination that can receive messages, such as mobile device identifier, or mobile phone number. Let's keep it simple and go with email.

1. Download the [example CSV file](/csv/segment.csv) and open it in a text editor on your computer.
1. Add a couple of users using the wildcard local parts notation you saw when you sent a test message.  
Example: If you verified `fred@domain`, then `fred+foo@domain`, `fred+bar@domain`, etc. will also work.
1. Save the file and remember its location. You will need this in the next step.

### Import a segment

You define the endpoints or user IDs that belong to your segment in a comma-separated values (CSV) or JSON file. Then, you import the file into Amazon Pinpoint to create the segment.

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

<!-- 
To learn more about segments, visit [Amazon Pinpoint Segments](https://docs.aws.amazon.com/pinpoint/latest/userguide/segments.html) in the Amazon Pinpoint User Guide.
-->
