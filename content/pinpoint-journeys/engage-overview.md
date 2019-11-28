---
title: "Engage overview"
weight: 30
---

Guide **Active users** through activities to **engage** with your product. All customers in this journey have engaged with your product before. They are part of the dynamic segment you created earlier. Get them to re-engage and spread the word about your product.

{{<mermaid align="center">}}
graph TD;

    10("Start")-- Segment: Active users --> 20("Wait 'X' hours")
    20 --> 30("Email: Nudge user to try<br/>one of our features<br>(virtual high 5!)")
    30 --> 40("Wait 'X' hours")
    40 --> 50{EmailCondition}
    50 -- Clicked link in email --> 60("Email:<br/>Send share/refer a friend")
    50 -- Opened email --> 70("Email:<br/>Send incentive to come back")
    50 -- Other --> 80("Email<br/>Last attempt")
    
    style 10 fill:#FF9900
    
{{< /mermaid >}}

### Message templates

Create four new email message templates. Each message is designed for its particular user engagement/activity. Follow the process you are already familiar with from the [Create a message template](/getting-started/create-a-message-template/) step.

1. Message template: *Nudge user to try one of our features*  
**Template name**: `Engage-ReEngage`  
**Subject**: `EngageUsers-ReEngage Email 1`  
**Message**: Copy/paste the [source code for the Engage-ReEngage email](/email-templates/engage-user-attempt-1.txt)

1. Message template: *Send share/refer a friend*  
**Template name**: `Engage-ReferAFriend`  
**Subject**: `EngageUsers-Refer A Friend`  
**Message**: Copy/paste the [source code for the Engage-ReferAFriend email](/email-templates/engage-user-attempt-2.txt)

1. Message template: *Send incentive to come back*  
**Template name**: `Engage-DiscountCode`  
**Subject**: `EngageUsers-Discount Code`  
**Message**: Copy/paste the [source code for the Engage-DiscountCode email](/email-templates/engage-user-attempt-3.txt)

1. Message template: *Last attempt*  
**Template name**: ```Engage-ReEngage2```  
**Subject**: ```EngageUsers-ReEngage Email 2```  
**Message**: Copy/paste the [source code for the Engage-ReEngage2 email](/email-templates/engage-user-final-attempt.txt)
