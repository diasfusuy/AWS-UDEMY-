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