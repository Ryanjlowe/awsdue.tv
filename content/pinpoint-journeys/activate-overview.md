---
title: "Activate overview"
weight: 50
---

Guide **Inactive users** through activities to **activate** them. No customers in this journey have engaged with your product. They are part of the dynamic segment you created earlier.

When a customer who visits your site in any part of this journey they become **active**. They exit the **Inactive users** segment and this journey. They join the **Active users** segment and start the **Engage active users** journey.

{{<mermaid align="center">}}
graph TD;

    10("Start")-- Segment: Inactive users --> 20("Wait 'X' hours")
    20 --> 50{SegmentCondition:<br/>Is user still inactive?}
    50 -- Yes --> 60("Email: Send incentive to come back")
    60 --> 70("Wait 'X' hours")
    70 --> 80{SegmentCondition:<br/>Is user still inactive?}
    80 -- Yes --> 90("Email: Offer help")
    
    style 10 fill:#FF9900
    
{{< /mermaid >}}

### Message templates

Create two new email message templates. Each message is designed for its particular user engagement/activity. Follow the process you are already familiar with from the [Create a message template](/getting-started/create-a-message-template/) step.

1. Message template: *Send incentive to come back*  
**Template name**: `Activate-DiscountCode`  
**Subject**: `Activate-Discount code`  
**Message**: Copy/paste the [source code for the Activate-DiscountCode email](/email-templates/activate-user-attempt-1.txt)

1. Message template: *Offer help*  
**Template name**: `Activate-OfferHelp`  
**Subject**: `Activate-Offer Help`  
**Message**: Copy/paste the [source code for the Activate-OfferHelp email](/email-templates/activate-user-attempt-2.txt)
