+++
title = "Activate user"
chapter = false
weight = 40
+++


In this Journey there are 2 different email templates that we are going to send your users to try get them to re-engage with your product. During this Journey if the user becomes an **Engaged user** (ie visits your site) they will exit this Journey and will move into the [Engage User Journey](/pinpoint-journeys/engage-users-journey/).


## Creating the message templates to send

Before we create the Journey we are going to two create new message templates following the same method we did in the previous section as we did in the [Getting Started](/getting-started/create-a-message-template/) section.

Create Message Template 1:  
   1. **Template name**: ```Activate-DiscountCode```  
   2. **Subject**: ```Activate-Discount code```  
   3. **Message**: Copy the html from the following <a href="/email-templates/activate-user-attempt-1.txt" target="_blank">link (will open new tab)</a>.

Create Message Template 2:  
   1. **Template name**: ```Activate-OfferHelp```  
   2. **Subject**: ```Activate-Offer Help```  
   3. **Message**: Copy the html from the following <a href="/email-templates/activate-user-attempt-2.txt" target="_blank">link (will open new tab)</a>.

## Building the Journey

From within the console on the left hand navigation bar click on "Journeys" and subsequently click on **Create Journey** on the top right hand side of the page.

![createJourney](/images/create-journey.png)

Before we start building the Journey lets give it a name by editing the box on the top right and call the Journey ```Activate Users```.
  
![createJourney](/images/iJourney-setup.png)

### 1. Journey Entry

The first stage of creating a Journey is defining the Journey Entry point, what it is that causes members to enter the Journey.

In this Journey we are going to use the **InActive Users** segment we created earlier and specify that we want new users to be added to the segment automatically every hour. In doing this it is possible to have Journeys run on a repeatable fashion without you needing to schedule the task. It is also possible to run the Journey as a 'One off' by choosing to never add new segment members.

1. Chose the **inactiveUsers** Segment
2. Specify to run once every **1 hours**
3. Click **Save**.

![createJourney](/images/iJourney-inactiveSegment.png)

### 2. Adding Activities

Users can now successfully enter the Journey.

1. Click on the **+** Symbol

![createJourney](/images/add-activity.png)

### 3. Wait

Within Pinpoint we give you the facility to perform a **Wait** stage, this means that instead of sending a number of emails concurrently we can specify we want the Journey to continue after a period of time or at a specific time.  

1) Click on the Plus symbol  
2) Choose **Wait**.  
3) Select **Period of Time**  
4) Set the amount of time to **1** hour  
5) Click **Save**  

![createJourney](/images/aJourney-wait.png)

### 4. Yes/No Split

We want to establish whether the user still remains in the **inactiveUsers** dynamic segment we created [earlier](/getting-started/create-a-dynamic-segment/). If they have left this segment the Journey for that user should end.

We will be performing a **Segment condition type** - this means we will be perform logic to determine if the user is in that segment.  

1. Select condition type **Segment**  
2. Chose the **inactiveUsers** segment.
3. Click **Save**.

![activeJourney](/images/iJourney-yesno.png)

### 5. Send Email

On the **"Yes"** branch we now want to send a followup email so we are going to send out the **Activate-DiscountCode** Message we configured earlier. 

1. Click on the Plus symbol below the green Yes box.   
2. Choose **Send email**.  
3. Select the **Activate-DiscountCode** template  
4. Choose Sender email address configured in the Getting started Lab  
5. Click **Save**

![createJourney](/images/iJourney-send-discount.png)

If the user is **NOT** in the inacetiveUsers segment we want the Journey to end so we will not add a step below the red No box. The user Journey will end.  

### 6. Add subsequent Inactive User steps

Following the same process as 5 & 6 introduce another Yes/No Split as a consequence of a Segment condition for the **Activate-OfferHelp** email.

## Complete Journey

Once you have completed all of the steps above your Journey should resemble the below image
![activeJourney](/images/iJourney-complete.png)

### Review and Publish

If you have successfully followed the above steps you will now be in a position to publish your Journey. At the top right of the screen click on Review.
![activeJourney](/images/aJourney-review_first.png)

If there are any errors you will be given a message to explain where to fix in your Journey, if not your Journey will be ready to go, click on Next.
![activeJourney](/images/aJourney-review.png)

You can now click **Publish**, once you publish a Journey you can no longer edit it. You are able to duplicate a flow if you do want to modify it in the future. Click on Publish - you are done!

![activeJourney](/images/aJourney-publish.png)

