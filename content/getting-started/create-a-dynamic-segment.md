+++
title = "Create a dynamic segment"
chapter = false
weight = 55
+++

A dynamic segment is a subset of a [Segment](/getting-started/create-a-segment/). In the previous section we uploaded a csv with a column labeled `User.UserAttributes.isActive`. We are going to create a dynamic segments based on this column. It is possible to create multifaceted dynamic segments but in this example we are going to just use this one column.

First of all leave the segment to "Build a Segment" and give the segment name as `activeUsers`
![createJourney](/images/dynamic-build.png)

From within the Segment Group section follow the steps:
1. Leave include endpoints at `any`
2. Chose the segment you created during the `Create a Segment` [section](/getting-started/create-a-segment/)
3. Add a filter by `user`
4. Chose the attribute `isActive` 
5. Set the value to `True`

![createJourney](/images/dynamic-segment-filter.png)

Click `Create Segment`

For the later workshops you will also require an `inactiveUsers` segment

1. Leave include endpoints at `any`
2. Chose the segment you created during the `Create a Segment` [section](/getting-started/create-a-segment/)
3. Add a filter by `user`
4. Chose the attribute `isActive` 
5. Set the modal operator to `is not`
6. Set the value to `True`

Click `Create Segment`
