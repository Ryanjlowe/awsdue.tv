+++
title = "Engage active users"
chapter = false
weight = 40
+++

## Building the Journey

In the [Amazon Pinpoint Console](https://console.aws.amazon.com/pinpoint/), navigate to **Journeys**. Click on **Create Journey**.

![createJourney](/images/create-journey.png)

Before you build the journey, give it a name by editing the box on the top right. Call the Journey **Engage Users**.

![createJourney](/images/aJourney-create-journey.png)  

{{% notice note %}}
Journeys will be autosaved as you progress through so you do not need to worry about saving mid flow.
{{% /notice %}}

### 1. Journey Entry

The first stage of creating a Journey is defining the **Journey Entry point**. This is what cause a user to enter the Journey.

In this Journey we are going to use the **activeUsers** segment we created earlier in the [Create Dynamic Segment](/getting-started/create-a-dynamic-segment/) section of the workshop and specify that we want new users to be added to the segment automatically every hour. 

1. Chose the **activeUsers** Segment
2. Specify to run once every **1 hours**
3. If you add a helpful description when the flow item in the Journey folds up in the interface you can read a description of what that flow was doing. Enter `Enter the Active User Dynamic Segment`.
4. Click **Save**

![createJourney](/images/aJourney-createEntry.png)

#### 2. Adding Activities

Users can now successfully enter the Journey. To add subsequent steps to the Journey simply click on the **+** symbol and you will be able to chose the type of activity you wish to build.
![createJourney](/images/add-activity.png)

#### 3. Wait

Within Pinpoint we give you the facility to perform a "Wait" stage, this means that instead of sending a number of emails concurrently we can specify we want the Journey to continue after a period of time or at a specific time. 

1) Click on the Plus symbol  
2) Choose **Wait**.  
3) Select **Period of Time**  
4) Set the amount of time to **1** hour  
5) Click **Save**  

![createJourney](/images/aJourney-wait.png)

#### 4. Send Email

Once the wait time has been completed the Journey continues. for the purpose of this workshop we are going to send out the **Engage-ReEngage** Message we configured earlier.  Click on the Plus symbol and chose **Send email**.

1) Select the **Engage-ReEngage** template  
2) Choose Sender email address configured in the Getting started Lab    
3) Click **Save**

![createJourney](/images/aJourney-send-email.png)

#### 5. Wait

Following sending an email you are likely to want to pause before you do followup activity - as with step 3 introduce another wait state to the Journey.

1) Click on the Plus symbol  
2) Choose **Wait**.  
3) Select **Period of Time**  
4) Set the amount of time to **1** hour  
5) Click **Save**  
![createJourney](/images/aJourney-wait.png)

#### 6. Multivariate Split

Within Journeys you can create a flow which is determined by certain criteria that can be defined in the flow. Within a **Multivariate split** the customer can go down one of up to four paths and an 'other' path.

In this Journey we will use a Multivariate split because we are going to send the user on the Journey based on one of three different criteria:  
A: **User clicked on links in email sent**  
B: **User Opened email**  
Other: **User did not engage with the email we sent**    

{{% notice note %}}
Within the Multivariate activity the user will **ONLY** take one of the paths and they will follow the highest letter path. In the above example someone who clicked on a link in an email will have also opened the email. In this scenario they would follow the path 'A - user clicked on links in email sent'. 
{{% /notice %}}
![activeJourney](/images/aJourney-mvt-split.png)

#### 6.1. Send Email

1. Click on the Plus symbol below **Branch A**  
2. Chose **Send email**.
3. Select the **Engage-ReferAFriend** template 
4. Choose Sender email address configured in the Getting started Lab
5. click **Save**  
![activeJourney](/images/aJourney-send-refer-email.png)

#### 6.2. Send Email

1. Click on the Plus symbol below **Branch B**  
2. Chose **Send email**.
3. Select the **Engage-DiscountCode** template 
4. Choose Sender email address configured in the Getting started Lab  
5. Click **Save**
![activeJourney](/images/aJourney-send-discount.png)

#### 6.3. Send Email

1. Click on the Plus symbol below **Else**  
2. Choose **Send email**  
3. Select the **Engage-ReEngage2** template and click **Save**
![activeJourney](/images/aJourney-send-reengage2.png)

### Complete Journey

Once you have completed all of the steps above your Journey should resemble the below image
![activeJourney](/images/aJourneyFull.png)

### Review and Publish

If you have successfully followed the above steps you will now be in a position to publish your Journey. At the top right of the screen click on Review.
![activeJourney](/images/aJourney-review_first.png)

If there are any errors you will be given a message to explain where to fix in your journey, if not your Journey will be ready to go, click on Next.
![activeJourney](/images/aJourney-review.png)

You can now click **Publish**, once you publish a Journey you can no longer edit it. You are able to duplicate a flow if you do want to modify it in the future. Click on Publish - you are done!

![activeJourney](/images/aJourney-publish.png)

### Understand Journey Analytics

After you click publish for the first time you will be presented a walkthrough of how you can review analytics and the status of your analytics. Review this content to dive deeper on the type of data that can be retrieved. This information is all available via API calls as well.
