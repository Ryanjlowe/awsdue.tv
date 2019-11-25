+++
title = "Activate user"
chapter = false
weight = 30
+++


In this journey we have 3 different email templates we are going to send depending on whether the user re-engages with the site. In this journey, if at any point the user engages with the site they will become an "Active" user and will then start flowing through the Active journey we created previously.

## Creating the message templates to send
Before we create the Journey we are going to two create new message templates following the same method we did in the previous section

Create Message Template 1:  
   1.  **Template name**: ```Inactive-DiscountCode```  
   2.  **Subject**: ```Inactive-Discount code```  
   3.  **Message**: Copy the html from the following link.  

Create Message Template 2:    
   1.  **Template name**: ```Inactive-OfferHelp```  
   2.  **Subject**: ```Inactive-Offer Help```  
   3.  **Message**: Copy the html from the following link.  



## Building the Journey

From within the console on the left hand navigation bar click on "Journeys" and subsequently click on `Create Journey` on the top right hand side of the page.

![createJourney](/images/create-journey.png)

Before we start building the Journey lets give it a name by editing the box on the top right and call the Journey `Inactive Users`.
  
![createJourney](/images/iJourney-setup.png).  

### 1. Journey Entry

The first stage of creating a Journey is defining the Journey Entry point, what it is that causes members to enter the journey.

In this journey we are going to use the `InActive Users` segment we created earlier and specify that we want new users to be added to the segment automatically every hour. In doing this it is possible to have Journeys run on a repeatable fashion without you needing to schedule the task. It is also possible to run the Journey as a 'One off' by choosing to never add new segment members.

1. Chose the `inactiveUsers` Segment
2. Specify to run once every `1` `hours`
3. If you add a helpful description when the flow item in the Journey folds up in the interface you can read a description of what that flow was doing. Enter `Enter the Inactive User Dynamic Segment`.
4. Click `Save`

![createJourney](/images/iJourney-inactiveSegment.png).

### 2. Adding Activities

Users can now successfully enter the Journey. To add subsequent steps to the journey simply click on the + symbol and you will be able to chose the type of activity you wish to build.

![createJourney](/images/add-activity.png)

### 3. Wait

Within Pinpoint we give you the facility to perform a "Wait" stage, this means that instead of sending a number of emails concurrently we can specify we want the journey to continue after a period of time or at a specific time. Click on the Plus symbol and chose ```Wait```.

![createJourney](/images/aJourney-wait.png)

### 4. Wait

Following sending an email you are likely to want to pause before you do followup activity - as with step 3 introduce another wait state to the Journey.

![createJourney](/images/aJourney-wait.png)

### 5. Yes/No Split

In the previous section we added a Multivariate split to allow multiple paths through based on the condition. For this journey we want to establish whether the user still remains in the `inactiveUsers` dynamic segment. If they have left the segment the journey for that user should end.

We will be performing a "Segment" condition - this means we will be perform logic to determine if the user is in that segment.  Select condition type `Segment` and chose the `inactiveUsers` segment.

![activeJourney](/images/iJourney-yesno.png)

### 6. Send Email

On the "Yes" branch we now want to send a followup email  so we are going to send out the ```Inactive-DiscountCode``` Message we configured earlier.  Click on the Plus symbol and chose ```Send email```.

Select the ```Inactive-DiscountCode``` template and click `Save`

![createJourney](/images/iJourney-send-discount.png)

We will leave the "No" branch empty and the user journey ends.  

### 7. Add subsequent Inactive User steps

Following the same process as 5 & 6 introduce another Yes/No Split as a consequence of a Segment condition for the ```Inactive-OfferHelp``` email.

## Complete Journey

Once you have completed all of the steps above your journey should resemble the below image
![activeJourney](/images/iJourney-complete.png)

### Review and Publish

If you have successfully followed the above steps you will now be in a position to publish your journey. At the top right of the screen click on Review.
![activeJourney](/images/aJourney-review_first.png)

If there are any errors you will be given a message to explain where to fix in your journey, if not your journey will be ready to go, click on Next.
![activeJourney](/images/aJourney-review.png)

You can now click `Publish`, once you publish a journey you can no longer edit it. You are able to duplicate a flow if you do want to modify it in the future. Click on Publish - you are done!

![activeJourney](/images/aJourney-publish.png)