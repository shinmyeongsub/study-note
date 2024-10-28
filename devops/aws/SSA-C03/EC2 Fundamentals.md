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

### Introduction to Security Groups
- Security Groups are the fundamental of network security in AWS
- They control how traffic is aalowed into or out of our EC2 Instances.
- Security groups only contain proves them over time <span style="color:green">allow</span> rules
- Security groups rules can reference by IP or by security group

### Security Groups Deeper Dive
- Security groups are acting as a "firewall" on EC2 instances
- They regulate : 
  - Access to Ports
  - Authorised IP ranges - IPv4 and IPv6
  - Control of inbound network (from other to the instance)
  - Control of outbound nework (from the instance to other)

### Security Groups Good to know
- Can be attached to multiple instances
- Locked down to a region / VPC combination
- Does live "outside" the EC2 - if traffic is blocked the EC2 instance won't see it
- <span style="color:skyblue">It's good to maintain one separate security group for SSH access</span>
- If your application is not accessible (time out), then it's a security group issue
- if you application gives a "connection refuse" error, then it's an application error or it's not launched
- All inbound traffic is <span style="color:red">blocked</span> by default
- All outbound traffic is <span style="color:green">authorised</span> by default

### Classic Ports to know
- 22 = SSH (Secure Shell) - log into a Linux instance
- 21 = FTP (File Transfer Protocol) - upload files into a file share
- 22 = SFTP (Secure File Transfer Protocol) - upload files using SSH
- 80 = HTTP - access unsecured websites
- 443 = HTTPS - access secured websites
- 3389 = RDP (Remote Desktop Protocol) - log into a Windows instance

### SSH troubleshooting
- **Student have the most problems with SSH**
- If things don't work...
  - Re-watch the lecture. You may have missed something
  - Read the troubleshooting guide
  - Try EC2 Instance Connect

- **<u>If one method works (SSH, Putty or EC2 Instance Connect) you're good</u>**
- If no method works, that's okay, the course wont't use SSH much 

### How to SSH into your EC2 Instance (Linux / Mac OS)
- We'll learn how to SSH into your EC2 instance using Linux / Mac
- SSH is one of the most important function. It allows you to control a remote machine, all using the command line

### EC2 Instances Purchasing Options
- **On-Demand Instances** - short workload, predictable pricing, pay by second
- **Reserved** (1 & 3 years)
  - Reserved Instances - long workloads
  - Convertible Reserved Instances - long workloads with flexible instances
- **Savings Plans** (1 & 3 years) - commitment to an amount of usage, long workload
- **Spot Instances** - short workloads, cheap, can lose instances (less reliable)
- **Dedicated Hosts** - book an entire physical server, control instance placement
- **Dedicated Instances** - no other customers will share your hardware
- **Capacity Reservations** - reserve capacity in a specific AZ for any duration

### EC2 On Demand ###
- Pay for what you use :
  - Linux or Windows - billing per second, after the first minute
  - All other operating systems - billing per hour
- Has the highest cost but no upfront payment
- No long-term commitment

- Recommended for **short-term** and **un-interrupted workloads**, where you can't predict how the application will behave

### EC2 Reserved Instances
- Up to <span style="color:skyblue">72%</span> discount compared to On-demand
- You reserve a specific instance attributes **(Instance Type, Region, Tenancy, OS)**
- **Reservation Period** - **1 year (+discount) or 3 years (+++discount)**
- **Payment Options** - **No Upfront (+), Partial Upfront (++), All Upfront (+++)**
- **Reserved Instance's Scope - Regional** or **Zonal** (reserve capacity in an AZ)
- Recommended for steady-state usage applications (think database)
- You can buy and sell in the Reserved Instance Marketplace

- **Convertible Reserved Intance**
  - Can change the EC2 instance type, instance family, OS, scope and tenancy
  - Up to <span style="color:skyblue">66%</span> discount.

### EC2 Savings Plans
- Get a discount based on long-term usage (up to 72% - same as RIs)
- Commit to a certain type of usage ($10/hour for 1 or 3 years)
- Usage beyond EC2 Savings Plans is billed at the On-Demand price

- Locked to a specific instance family & AWS region (e.g., M5 in us-east-1)
- Flexible across :
  - Instance Size (e.g., m5.xlarge, m5.2xlarge)
  - OS (e.g., Linux, Windows)
  - Tenancy (Host, Dedicated, Default)

### EC2 Spot Instances
- Can get a **discount of up to 90%** compared to On-demand
- Instances that you can "lose" at any point of time if your max price is less than the current spot price
- the **MOST cost-efficient** instances in AWS

- **Useful for workloads that are resilient to failure**
  - Batch jobs
  - Data analysis
  - Image processing
  - Any **distributed** workloads
  - Workloads with a flexible start and end time

- **Not suitable for critical jobs or databases**

### EC2 Dedicated Hosts
- A physical server with EC2 instance capacity fully dedicated to your use
- Allows you address **compliance requirements** and **use your existing server-bound software licenses** (per-socket, per-core, pe-- VM software licenses)
- Purchasing Options:
  - **On-demand** - pay per second for active Dedicated Host
  - **Reserved** - 1 or 3 years (No Upfront, Partial Upfront, All Upfront)
- The most expensive option

- Useful for software that have complicated licensing model (BYOL - Bring Your Own License)
- Or for companies that have strong regulatory or compliance needs

### EC2 Dedicated Instances
- Instances run on hardware that's dedicated to you
- May share hardware with other instances in same account
- No control over instance placement (can move hardware after Stop / Start)

### EC2 Capacity Reservations
- Reserve **On-Demand** instances capacity in a specific AZ for any duration
- You always have access to EC2 capacity when you need it
- **No time commitment** (create/cancel anytime), **no billing discounts**
- Combine with Regional Reserved Instances and Savings Plans to benefit from billing discounts
- You're charged at On-Demand rate whether you run instances or not
- Suitable for short-term, uninterrupted workloads that needs to be in a specific AZ

### EC2 Spot Instance Requests
- Can get a discount of up to 90% compared to On-demand
- Define <strong>max spot price</strong> and get the instance while <strong>current spot price < max</strong>
  - The hourly spot price varies based on offer and capacity
  - If the current spot price > your max price you can choose to <strong>stop</strong> or <strong>terminate</strong> your instance with a 2 miniutes grace period.
- Other strategy: <strong>Spot Block</strong>
  - "block" spot instance during a specified time frame (1 to 6 hours) without interruptions
  - In rare situations, the instance may be reclaimed
  - ---
  Spot Blocks are no longer avilable to new AWS customers since July 1st 2021 And won't be supported after December 31 2022

  Still, they *might* appear in the exam, so I won't remove this slide yet

  ---

- **Used for batch jobs, data analysis, or workload that are resilient to failures.**
- **Not great for critical jobs or databases**

### Spot Fleets
- Spot Fleets = set of Spot Instances + (optional) On-Demand Instances
- The Spot Fleet will  try to meet the target capacity with price constraints
  - Define possible launch pools : instance type (m5.large), OS, Availability Zone
  - Can have multiple launch pools, so that the fleet can choose
  - Spot Fleet stops launching instances when reaching capacity or max cost
- Strategies to allocate Spot Instances:
  - **lowestPrice:** from the pool with the lowest price (cost optimization, short workload)
  - **diversified:** distributed across all pools (great for availability, long workloads)
  - **capacityOptimized:** pool with the optimal capacity fro the number of instances
  - **priceCapacityOptimized (recommended):** pools with highest capacity available, then select the pool with the lowest price (best choice for most workloads)
- **<u>Spot Fleets allow ust to automatically request Spot Instances with the lowest price</u>**