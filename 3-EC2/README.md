### EC2 Elastic Compute Cloud
- Amazon EC2 stands for Elastic Compute Cloud and provides Infrastructure as a Service (IaaS).
- EC2 includes multiple components: EC2 instances, EBS volumes, Elastic Load Balancers, and Auto Scaling Groups (ASG).
- When launching an instance you choose the OS, CPU, RAM, storage type (EBS/EFS or instance store), and networking options.
- EC2 User Data allows bootstrapping: it runs once at first boot with root (sudo) privileges to automate initialization tasks. (Bootstrapping a server is just like “downloading and setting up a prebuilt project”. Except you’re setting up the entire machine automatically so it’s ready to run your app.)

