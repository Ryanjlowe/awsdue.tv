+++
title = "Engage user"
chapter = false
weight = 20
+++


In this Journey we have 4 different email templates we are going to send depending on user engagement/activity. We believe anyone in this Journey has engaged with your product before as they are part of a dynamic segment we created earlier.  We are trying to get them to re-engage and spread the word about your product.

We are going to be building out the left hand side of our flow diagram [here](/pinpoint-journeys/create-journeys/).

## Creating the message templates to send


Before we create the Journey we are going to create new message templates required for the emails. We will follow the same process as we did in the [Getting Started](/getting-started/create-a-message-template/) section

Create Message Template 1:  
   1.  **Template name**: ```Active-ReEngage```  
   2.  **Subject**: ```ActiveUsers-ReEngage Email 1```  
   3.  **Message**: Copy the html from the following <a href="/email-templates/activate-user-attempt-1.txt" target="_blank">link (will open new tab)</a>.

Create Message Template 2:    
   1.  **Template name**: ```Active-ReferAFriend```  
   2.  **Subject**: ```ActiveUsers-Refer A Friend```  
   3.  **Message**: Copy the html from the following link.  <a href="/email-templates/activate-user-attempt-2.txt" target="_blank">link (will open new tab)</a>

Create Message Template 3:    
   1.  **Template name**: ```Active-DiscountCode```  
   2.  **Subject**: ```ActiveUsers-Discount Code```  
   3.  **Message**: Copy the html from the following  <a href="/email-templates/activate-user-attempt-3.txt" target="_blank">link (will open new tab)</a>


Create Message Template 4:  
   1.  **Template name**: ```Active-ReEngage2```  
   2.  **Subject**: ```ActiveUsers-ReEngage Email 2```  
   3.  **Message**: Copy the html from the following <a href="/email-templates/activate-user-final-attempt.txt" target="_blank">link (will open new tab)</a> 

## Building the Journey

From within the console on the left hand navigation bar click on "Journeys" and subsequently click on **Create Journey** on the top right hand side of the page.

![createJourney](/images/create-journey.png)


Before we start building the Journey lets give it a name by editing the box on the top right and call the Journey **Active Users**.
  
![createJourney](/images/aJourney-create-journey.png).  

### 1. Journey Entry

The first stage of creating a Journey is defining the **Journey Entry point**. This is what causes users to enter the Journey.

In this Journey we are going to use the **Active Users** segment we created earlier in the [Create Dynamic Segment](/getting-started/create-a-dynamic-segment/) section of the workshop and specify that we want new users to be added to the segment automatically every hour. In doing this it is possible to have Journeys run on a repeatable fashion without you needing to worry about scheduling tasks.

1. Chose the **activeUsers** Segment
2. Specify to run once every **1 hours**
3. If you add a helpful description when the flow item in the Journey folds up in the interface you can read a description of what that flow was doing. Enter `Enter the Active User Dynamic Segment`.
4. Click **Save**

#### 2. Adding Activities

Users can now successfully enter the Journey. To add subsequent steps to the Journey simply click on the + symbol and you will be able to chose the type of activity you wish to build.
![createJourney](/images/add-activity.png)

There are a number of different activities you can chose from as stages in the Journey:

![createJourney](/images/journey-activities.png)

#### 3. Wait

Within Pinpoint we give you the facility to perform a "Wait" stage, this means that instead of sending a number of emails concurrently we can specify we want the Journey to continue after a period of time or at a specific time. Click on the Plus symbol and chose **Wait**.

![createJourney](/images/aJourney-wait.png)

#### 4. Send Email

Once the wait time has been completed the Journey continues for the purpose of this workshop we are going to send out the **Active-ReEngage** Message we configured earlier.  Click on the Plus symbol and chose **Send email**.

Select the **Active-ReEngage** template and click **Save**

![createJourney](/images/aJourney-send-email.png)

#### 5. Wait

Following sending an email you are likely to want to pause before you do followup activity - as with step 3 introduce another wait state to the Journey.

![createJourney](/images/aJourney-wait.png)

#### 6. Multivariate Split

Within Journeys you can create a flow which is determined by certain criteria that can be defined in the flow. With a Multivariate split the customer can go down one of up to four paths and an 'other' path. We do offer a other ways to navigate via user/engagement criteria (Yes/No Split, Random Split).

In this example we will use a multivariate split because we are going to send the user on the Journey based on one of three different criteria:  
A: **User clicked on links in email sent**  
B: **User Opened email**  
Other: **User did not engage with the email we sent**    

{{% notice note %}}
Within the Multivariate activity the user will ONLY take one of the paths and they will follow the highest letter path. In the above example someone who clicked on a link in an email will have also opened the email. In this scenario they would follow the path 'A - user clicked on links in email sent'. It's worth noting that if you have 'User opened email' as your first criteria even if the user clicked on a link they would never follow that path.
{{% /notice %}}
![activeJourney](/images/aJourney-mvt-split.png)

#### 6.1. Send Email

1. Click on the Plus symbol below **Branch A**  
2. Chose **Send email**.
3. Select the **Active-ReferAFriend** template and click **Save**  
![activeJourney](/images/aJourney-send-refer-email.png)

#### 6.2. Send Email

Click on the Plus symbol below **Branch b** and chose **Send email**.

Select the **Active-DiscountCode** template and click **Save**
![activeJourney](/images/aJourney-send-discount.png)

#### 6.3. Send Email

Click on the Plus symbol below **Else** and chose **Send email**.

Select the **Active-ReEngage2** template and click **Save**
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

