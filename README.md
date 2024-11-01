# Configuring-an-Amazon-CloudFront-Distribution-with-an-Amazon-S3-Origin

## Project Overview

In this project, I configured an Amazon CloudFront distribution with an Amazon Simple Storage Service (S3) bucket origin to deliver content securely and efficiently. By setting up CloudFront in front of the S3 bucket and securing it using Origin Access Control (OAC), I ensured that only CloudFront can access the S3 bucket. This setup is ideal for delivering static content with low latency and high transfer speeds, as well as enforcing secure access.

## Objectives

Through this lab, I achieved the following objectives:
- Created an Amazon S3 bucket with appropriate security settings.
- Configured the S3 bucket to enable controlled access.
- Added the S3 bucket as an origin to an existing CloudFront distribution.
- Secured the bucket to permit access exclusively through the CloudFront distribution.
- Configured OAC to enhance security and prevent direct access to the S3 bucket.
- Updated Amazon S3 resource policies for controlled access.

## Project Architecture
![CloudFront](https://github.com/user-attachments/assets/eda9c54d-3368-4409-944c-e512ee481c72)

## Project Tasks

### Task 1: Explore the Existing CloudFront Distribution

In this initial task, I reviewed the configuration of the pre-existing CloudFront distribution to understand its settings and layout.

- **Task 1.1**: Opened the CloudFront console.
- **Task 1.2**: Accessed the existing CloudFront distribution.
- **Task 1.3**: Reviewed and noted the properties of the CloudFront distribution, including caching behaviors, distribution ID, and origin settings.

### Task 2: Create an S3 Bucket

Here, I created a new S3 bucket to use as the CloudFront distribution's origin.

- Opened the S3 console and created a new bucket, ensuring that it was configured with the necessary security settings.

### Task 3: Configure the S3 Bucket for Public Access

To allow CloudFront to pull content, I configured the bucket for public access temporarily.

- **Task 3.1**: Enabled the bucket policy to allow the creation of public policies.
- **Task 3.2**: Configured a public read policy for the bucket to facilitate object access testing in the next steps.

### Task 4: Upload an Object and Test Public Access

Next, I uploaded a sample object to the bucket and tested public access to verify the bucket’s configuration.

- **Task 4.1**: Created a new folder in the bucket for organized storage.
- **Task 4.2**: Uploaded a test object (e.g., an image or document) into this folder.
- **Task 4.3**: Tested public access to the object using the S3 URL to ensure it was accessible.

### Task 5: Secure the Bucket with Amazon CloudFront and Origin Access Control

This task involved securing the S3 bucket so that only CloudFront could access it, restricting any direct public access.

- **Task 5.1**: Updated the bucket policy to permit access solely through the CloudFront distribution.
- **Task 5.2**: Enabled Amazon S3 public access blockers to prevent any unauthorized access.
- **Task 5.3**: Added the bucket as a new origin to the CloudFront distribution and set up Origin Access Control (OAC) for secure content delivery.
- **Task 5.4**: Configured a new behavior in CloudFront for the S3 origin to define caching and delivery rules.

### Task 6: Test Direct Access to the S3 Bucket

After securing the S3 bucket with CloudFront, I tested the direct access to confirm that access was denied via the S3 URL, ensuring secure delivery through CloudFront only.

### Task 7: Test Access to the Object Using CloudFront

Finally, I tested access to the S3 object using the CloudFront distribution URL to confirm that content could be accessed securely through CloudFront.

## Conclusion

By implementing CloudFront with an Amazon S3 origin, I created a secure, efficient solution for content distribution. The Origin Access Control (OAC) feature ensures that only CloudFront can access the S3 bucket, adding a robust layer of security to the architecture. This project demonstrates the value of using CloudFront to serve static content with enhanced performance and security.
