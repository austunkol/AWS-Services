# `AWS SDK Boto3`

## `What is Boto3`

- Boto3 is the AWS SDK (Software Development Kit) for Python.
- It enables you to create, use, update, and delete AWS resources with your Python scripts. It is basically a Python library.

## `Installation and Configuration`

- `pip install boto3`

- ` Note :` 
- If you are using Python3, try `pip3 install boto3 `instead. You must have pip/pip3 installed to be able to run the command.

## `Using Boto3`

- Open your Python interpreter and write the code.
- To be able to use Boto3, first you need to import it `(import boto3),` then you can type other commands regarding it.

```
import boto3

# Use Amazon S3
s3 = boto3.resource('s3')

# Print out all bucket names
for bucket in s3.buckets.all():
    print(bucket.name)
```

- let's try to upload a file to the S3 bucket.

```
import boto3

# Use Amazon S3
s3 = boto3.resource('s3')

# Upload a new file
data = open('test.jpg', 'rb')
s3.Bucket('my-bucket').put_object(Key='test.jpg', Body=data)
```