# Simple Scaling

You pick ANY Cloud Watch metric

For this and other examples in THIS POST I am choosing CPU Utilization

You specify, a SINGLE THRESHOLD beyond which you want to scale and specify your response

EXAMPLE: how many EC2 instances do you want to add or take away when the CPU UTILIZATION breaches the threshold.

The scaling policy then acts.

THRESHOLD - add 1 instance when CPU Utilization is between 40% and 50%

`NOTE: This is the ONLY Threshold`

# Step Scaling

You specify MULTIPLE thresholds Along with different responses.

Threshold A - add 1 instance when CPU Utilization is between 40% and 50%

Threshold B - add 2 instances when CPU Utilization is between 50% and 70%

Threshold C - add 3 instances when CPU Utilization is between 70% and 90%

And so on and so on

`Note: There are multiple thresholds`

# Target Tracking Scaling

You don't want to have to make so many decisions

Makes the experience simple as compared to the previous 2 scaling options

It’s automatic

All you do is pick CPU Utilization(Your metric and example for this post)

Set the value and that’s it

Auto scaling does the rest adding and removing the capacity in order to keep your metric(CPU utilization) as close as possible to the target value

It’s SELF OPTIMIZING

It means that it has an Algorithm that learns how your metric changes over time and uses that information to make sure that over and under scaling are minimized