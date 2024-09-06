# AWS-Serverless-Image-Processing-project-
ImageSculptor is a serverless image processing system using AWS services. It automates image resizing, compression, and format conversion via AWS Lambda, S3, and DynamoDB, ensuring scalable, efficient, and secure image management without infrastructure overhead.

# ImageSculptor - Serverless Image Processing with AWS

**ImageSculptor** is an image processing system built on AWS using serverless architecture. This project processes images through resizing, compressing, and converting to different formats using AWS Lambda, S3, and DynamoDB.

## Key Features:
- **Automatic Image Processing:** Resizes, compresses, and converts images on upload.
- **Serverless Architecture:** Powered by AWS Lambda, S3, and DynamoDB, ensuring scalability.
- **Efficient & Scalable:** No infrastructure management, allowing flexible scaling.
- **Metadata Management:** Stores processed image metadata in DynamoDB.
- **Secure:** Leverages AWS Identity and Access Management (IAM) for secure access control.

## Technologies Used:
- **Frontend:** AWS S3 (for image storage and retrieval).
- **Backend:** AWS Lambda (for image processing tasks).
- **Database:** DynamoDB (to store image metadata).
- **Storage:** Amazon S3 (to store and serve images).
- **Security:** AWS IAM for role-based security.

## Prerequisites:
- AWS account with configured IAM roles.
- AWS CLI installed and configured.
- S3 bucket and DynamoDB table created.
  
## Getting Started:
### 1. Clone the repository:
```bash
git clone https://github.com/andrewnguyen41/aws-serverless-image-processing
cd aws-serverless-image-processing
2. Set up the environment:
Create a .env file with your AWS credentials and bucket name:

AWS_ACCESS_KEY_ID=your-access-key
AWS_SECRET_ACCESS_KEY=your-secret-key
AWS_REGION=your-region
S3_BUCKET_NAME=your-bucket-name

3. Deploy the Lambda function:
Use AWS CLI or the AWS Console to deploy the Lambda function:

aws lambda create-function --function-name ImageSculptorFunction --runtime nodejs14.x --role arn:aws:iam::your-role --handler index.handler --zip-file fileb://function.zip
4. Upload an image:
Upload an image to the S3 bucket and trigger the Lambda function. The processed image will be available in the output bucket, and metadata will be stored in DynamoDB.

5. Monitoring:
Use AWS CloudWatch to monitor the performance and logs of your Lambda function.

Future Enhancements:
Add more image filters (grayscale, sepia, etc.).
Implement caching with AWS CloudFront.
Extend support for more file types.
