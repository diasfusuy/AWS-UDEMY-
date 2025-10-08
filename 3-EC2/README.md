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
