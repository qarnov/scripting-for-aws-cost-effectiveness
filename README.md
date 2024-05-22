# Scripting-for-aws-cost-effectiveness

One effective way to manage and reduce AWS cloud costs is by identifying and eliminating unused resources. In this example, we'll create a Lambda function to detect EBS snapshots that are no longer linked to any active EC2 instances and remove them, thereby saving on storage expenses.

## Project Description
Our goal is to develop a Lambda function that automates the identification and deletion of stale EBS snapshots. Here’s how it will work:

**Fetch EBS Snapshots:** The Lambda function will retrieve a list of all EBS snapshots owned by our AWS account.

**Get Active EC2 Instances:** It will also gather information on all active EC2 instances, including those in both running and stopped states.

**Check Snapshots:** For each EBS snapshot, the function will check if the associated volume is connected to any of these active instances.

**Delete Stale Snapshots:** If a snapshot is found to be detached from any active instance, the function will delete it to free up storage space and reduce costs.

By implementing this Lambda function, we can ensure that our storage resources are being used efficiently and avoid unnecessary expenditures on unused snapshots.
