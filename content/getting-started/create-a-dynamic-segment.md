+++
title = "Create a dynamic segment"
chapter = false
weight = 55
+++

You can create two types of segments in Amazon Pinpoint. In the last section you have imported a segment from a CSV file. **Imported segments** are static, i.e. they never change. 
**Dynamic segments** are based on attributes that you define and can change over time. When you add new endpoints to Amazon Pinpoint, or if you modify or delete existing endpoints, the number of endpoints in your dynamic segment may increase or decrease.

In this section you will use an imported segment as a base segment, and then refine it by adding filters.

The user list you uploaded contained a column labeled `User.UserAttributes.isActive`. This sets the `isActive` attribute of each `user` row. In your sample, `isActive` can be TRUE or FALSE.

### "Active users" segment

To create a dynamic segment that contains only active users, filter all users whose isActive attribute is TRUE.

1. Navigate to your project in the [Amazon Pinpoint Console](https://console.aws.amazon.com/pinpoint/), then **Segments**.

1. Choose **Create a segment**.

1. This time, select **Build a segment**. Enter a descriptive name for the segment that will contain your active users. 
![createJourney](/images/dynamic-build.png)

1. Configure **Segment Group 1** to add segment filters.
    1. Start with the imported segment you created in the previous [Create a Segment](../create-a-segment/) step.
    1. Select **Filter by user**.
    1. Filter all users where the user attribute **isActive** is **TRUE**.
    ![user attribute isActive is TRUE](/images/dynamic-segment-filter.png)

1. Click **Create Segment** to create your first dynamic segment.

### "Inactive users" segment

In the next chapter of the workshop you will also need a segment for users who are not active. Following the steps above to create a dynamic segment, create a second dynamic segment for users who are not active.  
This time, configure these segment filters:

1. Start with the imported segment you created in the previous [Create a Segment](../create-a-segment/) step.

1. Select **Filter by user**.

1. Filter all users where the user attribute isActive **is not** TRUE.
![user attribute isActive is not TRUE](/images/dynamic-segment-filter-is-not-active.png)

1. Click **Create Segment** to create the second dynamic segment.

You should now have three segments: the imported segment with all your users, and two dynamic segments, one for active, and one for inactive users.
