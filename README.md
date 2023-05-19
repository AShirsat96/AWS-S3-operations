# aws_s3_python
This is aws S3 connection using python BOTO. For creating this connection to the s3 client using Python i did not follow the AWS documentation.
In order to define the configuration you need to first define your AWS access key id, your secret access key, your region and what is your bucket name. After which you need to import BOTO 3.
My python version: python 3.8.8

1) Function for listing all my buckets: Post defining our configuration, we now write a function that can list all my buckets. First we need to connect to client and then we need to write a for loop to print the list of all my buckets.

2) Function for creating a new bucket with location constraint: Again first step in this function is connecting to the client. Post completion of this step, we write our loop for creating new bucket with a location constraint.

3) Function for uploading a new file to a specified bucket: First step in writing this function is connecting to the client. In order to upload the file we need to define the file to upload, the bucket name and the object name in our function.

4) Function for downloading a file from the bucket: There are two methods to download a file from a bucket. The first step of writing the function is again connecting to the client. While using this function, we need to mention the bucket name and the name of the object that has to be downloaded

5) Function for listing the objects in a specified bucket: While writing this function i first connected to the client and the wrote a FOR loop to print the list of objects within the specified bucket. While using this function, you will need to define the name of the specified bucket.

6) Function for deleting a specific file from a bucket: After connecting to the client, I have written a loop that will print the response meta data and also print out the HTTP status code. When you are using this function, you will need to define the specific bucket name and also specify the filepath of the file that is to be deleted.



