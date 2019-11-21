+++
title = "Active User Journey"
chapter = false
weight = 0
+++


- [ ] Update onboarding workflow.
- [ ] modify img path to /images" rahter than /images
- [ ] remove symlink
- [ ] dynamic segments - 'and who have used your app within the past 30 days.' also add content.
- [ ] ensure there is a message template section in pinpoint basics
- [ ] upload Message Templates
- [ ] remove journey exit from full diagram
- [ ] check that segments down stream can change once a journey has started
- [ ] inacurate total endpoints
- [ ] journey wait times.
- [ ] flow vs journey consistency
- [ ] clean up template creatiuon
## Journey Creation (Active Users)

In this section we are going to replicate a real life onboarding flow where we try to either "Re-engage" inactive users (see right hand red side of the diagram) by a sequence of emails or alternatively if the user is active on our site (see left hand side) we send a flow to get them to perform tasks which creates stickiness with the product.

![workflow](/images/OnboardingFlow_V1.png)

## Creating a Dynamic Segment

In order to be able to trigger the different Journeys we are going to use dynamic segments.

> Dynamic segments are based on the data that your apps provide to Amazon Pinpoint. When you create a dynamic segment, you choose the criteria that define that segment. For example, you could specify all customers who use version 2.0 of your app on an Android device, and who have used your app within the past 30 days. Amazon Pinpoint continuously re-evaluates your segments as your app records new customer interactions. As a result, the size and membership of each segment changes over time. For information about integrating your apps with Amazon Pinpoint, see Integrating Amazon Pinpoint with Your Application in the Amazon Pinpoint Developer Guide.

When we created the Segment in the previous section our data CSV contained UserAttributes that we are going to create a Dynamic Segment from, in this example the segment is fairly basic but you have the ability within Pinpoint to create multifaceted segments which can then be used to trigger the start of a journey.

### Create Active Users Segment

- [ ] get instructions


## Creating your first Journey - Active Users

In this journey we have 3 different email templates we are going to send depending on user engagement/activity. In the hypothetical section the user has engaged with our site before and we are trying to get them to re-engage and spread the word about the site

### Creating the message templates to send
Before we create the Journey we are going to create new message templates following the same method we did in the previous section


Create Message Template 1:  
   1.  **Template name**: ```Active-ReEngage```  
   2.  **Subject**: ```ActiveUsers-ReEngage Email 1```  
   3.  **Message**: Copy the html from the following link.  

Create Message Template 2:    
   1.  **Template name**: ```Active-ReferAFriend```  
   2.  **Subject**: ```ActiveUsers-Refer A Friend```  
   3.  **Message**: Copy the html from the following link.  

Create Message Template 3:  
   1.  **Template name**: ```Active-ReEngage2```  
   2.  **Subject**: ```ActiveUsers-ReEngage Email 2```  
   3.  **Message**: Copy the html from the following link.  

### Building the Journey

From within the console on the left hand navigation bar click on "Journeys" and subsequently click on `Create Journey` on the top right hand side of the page.

![createJourney](/images/create-journey.png)


Before we start building the Journey lets give it a name by editing the box on the top right and call the Journey `Active Users`.
  
![createJourney](/images/aJourney-create-journey.png).  

#### 1. Journey Entry

The first stage of creating a Journey is defining the Journey Entry point, what it is that causes members to enter the journey.

In this journey we are going to use the `Active Users` segment we created earlier and specify that we want new users to be added to the segment automatically every hour. In doing this it is possible to have Journeys run on a repeatable fashion without you needing to schedule the task. It is also possible to run the Journey as a 'One off' by choosing to never add new segment members.

1. Chose the `activeUsers` Segment
2. Specify to run once every `1` `hours`
3. If you add a helpful description when the flow item in the Journey folds up in the interface you can read a description of what that flow was doing. Enter `Enter the Active User Dynamic Segment`.
4. Click `Save`

![createJourney](/images/aJourney-createEntry.png).

#### 2. Adding Activities

Users can now successfully enter the Journey. To add subsequent steps to the journey simply click on the + symbol and you will be able to chose the type of activity you wish to build.
- [ ] add plus symbol image.

![createJourney](/images/journey-activities.png)

#### 3. Wait

Within Pinpoint we give you the facility to perform a "Wait" stage, this means that instead of sending a number of emails concurrently we can specify we want the journey to continue after a period of time or at a specific time. Click on the Plus symbol and chose ```Wait```.

- [ ] add details here - confirming how we will do the wait

![createJourney](/images/aJourney-wait.png)

#### 4. Send Email

Once the wait time has been completed the Journey continues for the purpose of this workshop we are going to send out the ```Active-ReEngage``` Message we configured earlier.  Click on the Plus symbol and chose ```Send email```.

Select the ```Active-ReEngage``` template and click `Save`

![createJourney](/images/aJourney-send-email.png)

#### 5. Wait

Following sending an email you are likely to want to pause before you do followup activity - as with step 3 introduce another wait state to the Journey.

- [ ] add details here - confirming how we will do the wait

![createJourney](/images/aJourney-wait.png)

#### 6. Multivariate Split

Within Journeys you can create a flow which is determined by certain criteria that can be defined in the flow. With a Multivariate split the customer can go down one of up to four paths and an 'other' path. We do offer a other ways to navigate via user/engagement criteria (Yes/No Split, Random Split).

In this example we will use a multivariate split because we are going to send the user on the journey based on one of three different criteria:
A. User clicked on links in email sent
B. User Opened email
Other. User did not engage with the email we sent. 

> Within the Multivariate activity the user will ONLY take one of the paths and they will follow the highest letter path. In the above example someone who clicked on a link in an email will have also opened the email. In this scenario they would follow the path 'A - user clicked on links in email sent'. It's worth noting that if you have 'User opened email' as your first criteria even if the user clicked on a link they would never follow that path.


- define condition types

![activeJourney](/images/aJourney-mvt-split.png)

#### 6.1. Send Email

Click on the Plus symbol below `Branch A` and chose ```Send email```.

Select the ```Active-ReferAFriend``` template and click `Save`
![activeJourney](/images/aJourney-send-refer-email.png)

#### 6.2. Send Email

Click on the Plus symbol below `Branch b` and chose ```Send email```.

Select the ```Active-DiscountCode``` template and click `Save`
![activeJourney](/images/aJourney-send-discount.png)

#### 6.3. Send Email

Click on the Plus symbol below `Else` and chose ```Send email```.

Select the ```Active-ReEngage2``` template and click `Save`
![activeJourney](/images/aJourney-send-reengage2.png)
### Complete Journey

Once you have completed all of the steps above your journey should resemble the below image
![activeJourney](/images/aJourneyFull.png)


![pinpointConsole](/images/samplejourney-separateemailbasedonsegment.png)
following one could use yes/no rather than mv so give an example of an MV split which could be if link click / if email open . if email delivered
![pinpointConsole]/images/samplejourney-separateemailbasedonsegment.png)

* create templates - only email supported at the moment
* 
* chose entry trigger
- [x] can we embed an SMS No. It’ll probably be next year. 


