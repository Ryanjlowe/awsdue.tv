+++
title = "Overview"
chapter = false
weight = 20
+++

{{% notice note %}}
The chapters in this workshop build on each other. Make sure you have completed the steps in [Getting Started](/getting-started/) before you continue.
{{% /notice %}}

In this real-life onboarding flow you distinguish between active users and inactive users.

Guide **Active users** through journey activities to **engage** with your product. Ideally they perform an activity that creates a deeper connection with your product, or helps them get familiar with a particular feature.

Guide **Inactive users** through journey activities to **activate** them.

{{<mermaid align="center">}}
graph TD;

    1("Start")-- Segment: Active users -->2("Journey: Engage active users")
    1 -- Segment: Inactive users -->12("Journey: Activate inactive users")

    style 1 fill:#FF9900
    
{{< /mermaid >}}

{{<mermaid align="center">}}
graph TD;

    1("Start")-- active users -->2("Wait 'X' hours")
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
