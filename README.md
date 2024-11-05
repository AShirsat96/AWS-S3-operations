# AWS S3 Operations

A Python implementation for basic AWS S3 operations using boto3. This implementation provides functions for listing, creating, uploading, downloading, and deleting S3 bucket contents.

## Prerequisites

- Python 3.8.19
- boto3 (AWS SDK for Python)
- AWS Account with S3 access
- AWS Access Key and Secret Access Key

## Installation

Install the required AWS SDK for Python:

```bash
pip install boto3
```

## Configuration

You'll need to configure the following AWS credentials:

```python
aws_accesskey = <Your Access Key>
aws_secretaccess = <Your secret access key>
myregion = <your region>
mybucket = <your bucket name>
```

## Required Libraries
```python
import boto3
import os
import logging
```

## Functions

### 1. List Buckets
Lists all S3 buckets in your AWS account.

```python
List_My_Buckets(aws_access, aws_secret, aws_region)
```

### 2. Create Bucket
Creates a new S3 bucket with location constraint.

```python
create_bucket(aws_access, aws_secret, aws_region, bucket_name)
```

### 3. Upload File
Uploads a file to specified S3 bucket.

```python
upload_file(aws_access, aws_secret, aws_region, bucket_name, file_toupload, object_name=None)
```
- If `object_name` is not specified, the filename will be used

### 4. Download File
Two methods are provided for downloading files:

Method 1 (using download_fileobj):
```python
download_file(aws_access, aws_secret, aws_region, bucket_name, file_todownload, object_name)
```

Method 2 (using download_file):
```python
download_file_2(aws_access, aws_secret, aws_region, bucket_name, file_todownload, object_name)
```

### 5. List Objects
Lists all objects in a specified bucket with their sizes in KB.

```python
list_object_v2(aws_access, aws_secret, aws_region, bucket_name)
```

### 6. Delete Object
Deletes a specific file from a bucket.

```python
delete_object(aws_access, aws_secret, aws_region, bucket_name, file_todelete)
```

## Error Handling

All functions include error handling using try-except blocks for ClientError exceptions and logging.

## Official Documentation References

- [Boto3 Documentation](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)
- [Boto3 S3 Documentation](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html)
