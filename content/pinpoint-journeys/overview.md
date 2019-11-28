+++
title = "Overview"
chapter = false
weight = 20
+++

In this section of the workshop we are going to build an advanced journey. In order to do this section you **MUST** complete the previous Amazon Pinpoint [Getting Started](/getting-started/) section as we will be using a number of these components.

We are going to replicate a real life onboarding flow where we try to either "Re-engage" inactive users (see right hand red side of the diagram) by a sequence of emails or alternatively if the user is active on our site (see left hand side) we send a flow to get them to perform tasks which creates stickiness with the product.

{{<mermaid align="center">}}
graph TD;

    1("Welcome email")-- active users -->2("Wait 'X' hours")
    2 --> 3("Nudge users to engage by trying <br>out one of our features<br>(virtual high 5!)")
    3 --> 4("Wait 'X' hours")
    4 --> 5{EmailCondition}
    5 --> 6(clicked)
    5 --> 7(opened)
    5 --> 8(other)
    6-->9("Send share/refer a friend email")
    7-->10("Send incentive to come back email")
    8-->11("?")
    1 -- inactive users -->12("Wait 'X' hours")
    12 --> 13("Re-affirm what our product does and <br>get them to become active")
    13 --> 14("Wait 'X' hours")
    14 --> 15{SegmentCondition}
    15 -- still inactive -->16("Send incentive to come back email")
    16 --> 17("Wait 'X' hours")
    17 --> 18{SegmentCondition}
    18 -- still inactive -->19("offer help")
    
    style 1 fill:#FF9900
    
{{< /mermaid >}}
