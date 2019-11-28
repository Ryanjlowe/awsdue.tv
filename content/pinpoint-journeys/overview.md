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

    A((Start)) -- Segment: Active users --> B(Journey:<br/>Engage active users)
    A -- Segment: Inactive users --> C(Journey:<br/>Activate inactive users)

    style A fill:#FF9900
    
{{< /mermaid >}}