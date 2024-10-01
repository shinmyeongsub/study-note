### Amazon S3 - Moving between Strage Classes
- You can transition objects between storage classes
- For infrequently accessed object, move them to **Standard IA**
- For archive objects that you don't need fast access to, move them to **Glacier or Glacier Deep Archive**
- Moving objects can be automated using a **Lifecycle Rules**

### Amazon S3 - Lifecycle Rules
- **Transition Actions** - configure objects to transition to another storage class
  - Move objects to Standard IA class 60 days after creation
  - Move to Glacier for archiving after 6 months
- **Expiration actions** - configure objects to expire (delete) after some time
  - Access log files can be set to delete after a 365 days
  - **Can be used to delete old versions of files (if versioning is enabled)**
  - Can be used to delete incomplete Multi-Part uploads
- Rules can be created for a certain prefix (example:s3://mybucket/mp3/*)
- Rules can be created for certain objects Tags (example:*Department:Finance*)

### Amazon S3 - Lifecycle Rules (Scenario 1)
- **Your application on EC2 creates images thumbnails after profile photos are uploaded to Amazon S3. These thumbnails can be easily recreated, and only need to be kept for 60 days. The source images should be able to be immediately retrieved for these 60 days, and afterwards, the user can wait up to 6 hours. How would yoou design this?

- S3 source images can be on **Standard**, with a lifecycle configuration to transition them to **Glacier** after 60 days
- S3 thumbnails can be on **One-Zone IA**, with a lifecycle configuration to expire them (delete them) after 60 days

### Amazon S3 - Lifecycle Rules (Scenario 2)
- **A rule in your company states that you should be able to recover your deleted S3 objects immediately for 30 days, although this may happen rerely. After this time, and for up to 365 days, deleted objects should be recoverable within 48 hours.**

- **Enable S3 Versioning** in order to have object versioons, so that "deleted objects" are in fact hidden by a "delete marker" and can be recovered
- Transition the "noncurrent versions" of the object to **Standard IA**
- Transition afterwards the "noncurrent verions" to **Glacier Deep Archive**

### Amazon S3 Analytics - Stroage Class Analysis
- Help you decide when to transition objects to the right storage class
- Recommendations for **Standard** and **Standard IA**
  - Does NOT work for One-Zone IA or Glacier
- Report is updated daily
- 24 to 48 hours to start seeing data analysis
- Good first step to put together Lifecycle Rules (or improve them)!

### S3 - Requester Pays
- In general, bucket owners pay for all Amazon S3 storage and data transfer costs associated with their bucket
- **With Requester Pays buckets**, the requester instead of the bucket owner pays the cost of the request and the data download from the bucket
- Helpful when you want to share large datasets with other accounts
- The requester must be authenticated in AWS (cannot be anonymous)

### S3 Event Notifications
- S3:ObjectCreated, S3:ObjectRemoved, S3:ObejctRestore, S3:Replication...
- Object name filtering possible (*.jpg)
- <u>Use case</u>: generate thumbnails of images uploaded to S3
- **Can create as many "S3 events" as desired**
- S3 event notifications typically deliver events in seconds but can sometimes take a minute or longer

### S3 Event Notifications with Amazon EventBridge
- **Advanced filtering** options with JSON rules (metadata, obejct size, name...)
- **Multiple Destinations** - ex Step Functions, Kinesis Streams / Firehose...
- **EventBridge Capabilities** - Archive, Replay Event, Reliable delivery

### S3 - Baseline Performance
- Amazon S3 automatically scales to high request rates, latency 100-200 ms
- Your application can achieve at least **3,500 PUT/COPY/POST/DELETE or 5,500 GET/HEAD requests per second per prefix in a bucket.**
- There are no limits to the number of prefixes in a bucket.
- <u>Example (object path => prefix)</u>
  - bucket/folder1/sub1/file => /folder1/sub1/
  - bucket/folder2/sub2/file => /folder2/sub2/
  - bucket/1/file => /1/
  - bucket/2/file => /2/ 

### S3 Performance
- **Multi-Part upload:**
  - recommended for files > 100MB, must use for files > 5GB
  - Can help parallelize uploads (speed up transfers)
- **S3 Transfer Acceleration**
  - Increase transfer speed by transferring file to an AWS edge location which will forward the data to the S3 bucket in the target region
  - Compatible with multi-part upload

### S3 Performance - S3 Byte-Range Fetches
- Parallelize GETs by requesting specific byte ranges
- Better resilience in case of failures

### S3 Batch Operations
- Perform bulk operations on existing S3 objects with a single request, example:
  - Modify obejct metadata & properties
  - Copy objects between S3 buckets
  - **Encrypt un-encrypted objects**
  - Modfiy ACLs, tags
  - Restore obejcts from S3 Glacier
  - Invoke Lambda function to operform custom action on each object
- A job consists of a list of objects, the action to perform, and optional parameters.
- S3 Batch Operations manages retires, tracks progress, sends completion notifications, generate reports ...

### S3 Batch Operations
- Perform bulk operations on existing S3 objects with a single request, example:
  - Modify object metadata & properties
  - Copy objects between S3 buckets
  - **Encrypt un-encrypted objects**
  - Modify ACLs, tags
  - Restore objects from S3 Glacier
  - Invoke Lambda function to perform custom action on each object
- A job consists of a list of objects, the action to perform, and optional parameters
- S3 Batch Operations manages retries, tracks progress, sends completion notifications, generate reports ...
- **You can use S3 Inventory to get object list and use S3 Select to filter your objects**

### S3-Strage Lens
- Understand, analyze, and optimize storage across entire AWS Organization
- Discover anomalies, identify cost efficiencies, and apply data protection best practices across entire AWS Organization (30 days usage & activity metrics)
- Aggregate data for Organization, specific accounts, regioons, buckets, or prefixes
- Default dashboard or create your own dashboards
- Can be configured to export metrics daily to an S3 bucket (CSV, Parquet)

### Storage Lens - Default Dashboard
- Visualize summarized insights and trends for both free and advanced metrics
- Default dashboard shows Multi-Region and Multi-Account data
- Preconfigured by Amazon S3
- Can't deleted, but can be disabled

### Stroage Lens - Metrics
- **Summary Metrics**
  - General insights about your S3 storage
  - StorageBytes, ObjectCount...
  - Use cases: identify the fastest-growing (or not used) buckets and prefixes
- **Cost-Optimization Metrics**
  - Provide insights to manage and optimize your storage costs
  - NonCurrentVersionStorageBytes, IncompleteMultipartUploadStroageBytes...
  - Use cases: identify buckets with incomplete multipart uploaded older than 7 days, Identify which objects could be transitioned to lower-cost storage class
- **Data-Protection Metrics**
  - Provide insights for data protection features
  - VersioningEnabledBucketCount, MFADeleteEnabledBucketCount, SSEKMSEnabledBucketCount, CrossRegionReplicationRuleCount...
  - Use cases: identify buckets that aren't following data-protection best practices
- **Access-management Metrics**
  - Provide insights for S3 Object Ownership
  - ObjectOwnershipBucketOwnerEnforcedBucketCount...
  - Use cases: identify which Object Ownership settings your buckets use
- **Event Metrics**
  - Provide insights for S3 Event Notifications
  - EventNotificationEnabledBucketCount (identify which buckets have S3 Event Notifications configured)
- **Performance Metrics**
  - Provide insights for S3 Transfer Acceleration
  - TransferAccelerationEnabledBucketCount (identify which buckets have S3 Transfer Acceleratioon enabled)
- **Activity Metrics**
  - Provide insights about how your storage is requested
  - AllRequests, GetRequests, PutRequests, ListRequests, BytesDownloaded...
- **Detailed Status Code Metrics**
  - Provide insights for HTTP status codes
  - 200OKStatusCount, 403ForbiddenErrorCount, 404NotFoundErrorCount...

### Storage Lens - Free vs Paid
- **Free Metrics**
  - Automatically available for all customers
  - Contains around 28 usage metrics
  - Data is available for queries for 14 days
- **Advanced Metrics and Recommendataions**
  - Additional paid metrics and features
  - **Advanced Metrics** - Activity, Advanced Cost Optimization, Advanced Data Protection, Status Code
  - **CloudWatch Publishing** - Access metrics in CloudWatch without additional charges
  - **Prefix Aggregation** - Collect metrics at the prefix level
  - Data is available for queries for 15 months