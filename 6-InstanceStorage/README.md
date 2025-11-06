## EC2 Instance Storage
Think of EBS Volumes as network USB sticks. It is like a USB stick that you can take from one computer and put into another, but you do not physically insert it into a computer. Instead, it is attached through the network.

EBS Volumes are network drives, not physical drives. Communication between the instance and the EBS Volume occurs over the network. Because of this, there may be some latency from one computer reaching another server.

Since EBS Volumes are network drives that can be detached from an EC2 instance and attached to another very quickly, they are extremely handy for scenarios such as failovers.

EBS Volumes are locked to a specific Availability Zone. As mentioned, if an EBS Volume is created in us-east-1a, it cannot be attached to us-east-1b. However, if we create a snapshot, we can move a volume across different Availability Zones.

Finally, EBS Volumes are volumes where you must provision capacity in advance. You need to specify how many gigabytes you want and the IOPS (Input/Output Operations Per Second). This defines how you want your EBS Volume to perform. You will be billed for the provisioned capacity, and you can increase the capacity over time to improve performance or size.  

### Key Takeaways
- EBS Volumes are Elastic Block Store network drives that persist data beyond instance termination.

- EBS Volumes can only be attached to one EC2 instance at a time and are bound to a specific Availability Zone.

- Snapshots enable moving EBS Volumes across different Availability Zones.

- The "delete on termination" attribute controls whether EBS Volumes are deleted when the associated EC2 instance is terminated.

## EBS Snapshot
- EBS snapshot allows to create point-in-time backups of your volumes.

- Snapshots can be copied across AWS regions to support disaster recovery.

-In different availibility zones, we can create new volumes from existing snapshots.

- With recycle bin feature snapshots deleted by accident can be recovered in retention period. 

# How to Launch EC2 and Install Apache HTTPD

1. Launching the Instance:

- Started an EC2 instance using Amazon Linux 2 and t2.micro type.

- Used an existing security group (launch wizard one) and added a user data script that installs Apache HTTPD, excluding the final line that creates an index file.

2. Installing Apache:

- Waited for the user data script to complete, as Apache installation takes 1–2 minutes even after the instance shows as “running.”

- Verified the installation by refreshing the public IP to see the Apache test page.

3. Creating an AMI:

- Created an Amazon Machine Image (AMI) named “demo image” from the configured instance to capture its current state.

- Waited for the AMI status to change from “pending” to “available.”

4. Launching from AMI:

- Launched a new instance using the created AMI from the “My AMIs” tab.

- Used simplified user data (only creating an index file) since Apache was already installed in the AMI.

- Verified that the new instance quickly displayed the “Hello World” web page.

5. Benefits of AMIs:

- AMIs allow you to save pre-configured environments (software, security tools, dependencies).

- Speeds up deployments by eliminating repetitive setup steps.

- Enables consistent, quick instance launches for testing, scaling, or production use.

6. Final Step:

- Terminated all instances to avoid charges.

Key Takeaway:
- Creating and using AMIs lets you replicate fully configured EC2 environments quickly and efficiently—making deployments faster and more consistent.