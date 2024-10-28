## AWS Global Infrastructure
- AWS Regions
- AWS Availability Zones
- AWS Data Centers
- AWS Edge Locations / Points of Presence

### AWS Regions
- AWS has <Strong>Regions</Strong> all around the world
- Names can be us-east-1, eu-west-3 ...
- A region is a <Strong>cluster of data centers</strong>
- <strong>Most AWS services are region-scoped</strong>

### How to choose an AWS Regions
- <Strong>Compliance with data governance and legal requirements</strong> : \
data never leaves a region without your explicit permission
- <Strong>Proximity to customers</strong> : reduced latency
- <Strong>Available services within a Region</Strong> : \
  new services and new features aren't available in every Region
- <Strong>Pricing</Strong> : pricing varies region to region and is transparent in the service pricing page

### AWS Availability Zones
- Each region has many availability zones (usually 3, min 3, max is 6)
- Each availability zone (AZ) is one or more discrete data centers with redundant power, networking, and connectivity
- They're connected with high bandwidth, ultra-low latencty networking

#### AWS has Global Services :
- Identity and Access Management (IAM)
- Route 53 (DNS Service)
- CloudFront (Content Delivery Network)
- WAF (Web Application Firewall)

#### Most AWS services are Region-scoped :
- Amazone EC2 (Infrastructure as a Service)
- Elastic Beanstalk (Platform as a Service)
- Lambda (Function as a Service)
- Rekognition (Software as a Service)