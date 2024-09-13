### Amazon EC2
- EC2 is one of the most popular of AWS' offering
- EC2 = Elastic Compute Cloud = Infrastructure as a Service
- It mainly consists in the capability of :
  - Renting virtual machines (EC2)
  - Storing data on virtual drives (EBS)
  - Distributing load across machines (ELB)
  - Scaling the services using an auto-scaling group (ASG)
- Knowing EC2 is fundamental to understand how the Cloud works

### EC2 sizing & configuration options
- Operating System (OS) : Linux, Windows or Mac OS
- How much compute power & cores (CPU)
- How much random-access memory (RAM)
- How much storage space :
  - Network-attached <strong>(EBS & EFS)</strong>
  - hardware <strong>(EC2 Instance Store)</strong>
- Network card : speed of the card, Public IP address
- Firewall rules : <strong>security group</strong>
- Bootstrap script (configure at first launch) : EC2 User Data

### EC2 User Data
- It is possible to bootstrap our instances using an EC2 User data script.
- <span style="color:skyblue">**bootstrapping**</span> means launching commands when a machine starts
- That script is <span style="color:skyblue">**only run once**</span> at the instance <span style="color:skyblue">**first start**</span>
- EC2 user data is used to automate boot tasks such as:
  - Installing updates
  - Installing software
  - Downloading common files from the internet
  - Anything you can think of
- The EC2 User Data Script runs with the root user

### Hands-On : Launching an EC2 Instance running Linux
- We'll be launching our first virtual server using the AWS Console
- We'll get a first high-level approach to the various parameters
- We'll see that our web server is launched using EC2 user data

### EC2 Instance Types - Overview
- AWS has the following naming convention
  - ex) <span style="color:skyblue">m</span><span style="color:yellow">5</span>.<span style="color:green">2xlarge</span>
    - <span style="color:skyblue">m</span> : instnace class
    - <span style="color:yellow">5</span> : generation (AWS improves them over time)
    - <span style="color:green">2xlarge</span> : size within the instance class

### EC2 Instance Types - General Purpose
- Great for a diversity of workloads such as web servers or code repositories
- Balance between :
  - Compute
  - Memory
  - Networking
- In the course, we will be using the t2.micro which is a General Purpose EC2 instance

### EC2 Instance Types - Compute Optimized
- Great for compute-intensive tasks that require high performance processors:
  - Batch processing workloads
  - Media transcoding
  - High performance web servers
  - High performance computing (HPC)
  - Scientific modeling & machine learning
  - Dedicated gaming servers

### EC2 Instance Types - Memory Optimized
- Fast performance for workloads that process large data sets in memory
- Use cases:
  - High performance, relational/non-relational databases
  - Distributed web scale cache stores
  - In-memory databases optimized for BI (business intelligence)
  - Applications performing real-time processing of big unstructured data

### EC2 Instance Types - Storage Optimized
- Great for storage-intensive tasks that require high, sequential read and write access to large data sets on local storage
- Use cases:
  - High frequency online transaction processing (OLTP) systems
  - Relational & NoSQL databases
  - Cache for in-memory databases (for example, Redis)
  - Data warehousing applications
  - Distributed file systems

