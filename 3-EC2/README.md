### EC2 Elastic Compute Cloud
- Amazon EC2 stands for Elastic Compute Cloud and provides Infrastructure as a Service (IaaS).
- EC2 includes multiple components: EC2 instances, EBS volumes, Elastic Load Balancers, and Auto Scaling Groups (ASG).
- When launching an instance you choose the OS, CPU, RAM, storage type (EBS/EFS or instance store), and networking options.
- EC2 User Data allows bootstrapping: it runs once at first boot with root (sudo) privileges to automate initialization tasks. (Bootstrapping a server is just like “downloading and setting up a prebuilt project”. Except you’re setting up the entire machine automatically so it’s ready to run your app.)

## Creating EC2 Instance
In the hands-on session, I launched EC2 instance and web server in the cloud. I explored power of speed and cloud, using API calls to start, stop, and manage instances.

- Key Takeaways
Launched EC2 instance using AWS console with Amazon Linux 2 AMI
- Conigured instance detailes including name tags, instance type, key pair, and security group.
- Used EC2 user data to run a script that installs and starts a web server on the instance.
- Learned how to start, stop, and terminate EC2 instance and understood the implications on public IP addres

## Shared Responsibility Model for EC2
- AWS is responsible for the security of the physical data centers and infrastructure.

- Users are responsible for security within the cloud, including configuring security groups and managing their EC2 instances.
- Users must maintain their operating system patches,updates, and installed software on EC2 instances.
- Proper assignment of IAM roles and securing data on EC2 instances are critical user responsibilities.

# Summary
- EC2 instances are composed of an AMI defining the operating system, instance size specifying CPU and RAM, storage, security groups as firewalls, and user data scripts for initialization.

- Security groups act as external firewalls to EC2 instances, controlling allowed ports and IP addresses.

- EC2 User Data scripts run at the first start of an instance to configure it, such as setting up a web server.

- SSH allows terminal access to EC2 instances on port 22, and EC2 instance roles enable instances to interact with IAM securely.

- Multiple EC2 purchasing options exist: on-demand, spot instances, reserved instances (standard or convertible), dedicated hosts, and dedicated instances.