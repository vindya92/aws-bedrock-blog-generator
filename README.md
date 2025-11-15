AWS Bedrock Blog Generator

A Python-based AI-powered blog/article generator using Amazon Bedrock and Claude / Llama models. This tool allows you to input a topic, tone, and target audience and instantly produce high-quality long-form content suitable for blogs, newsletters, or social posts.

 Project acrchitecture
 <img width="1212" height="756" alt="image" src="https://github.com/user-attachments/assets/65b6b796-4177-4b52-a432-5cc54d509530" />

 Features

✔ Generate full-length AI blogs using Amazon Bedrock
✔ Supports multiple writing tones (Professional, Friendly, Humorous, Technical, etc.)
✔ Custom target audience selection
✔ Outputs SEO-friendly blog content
✔ Configurable model ID (Claude, Llama, etc.)
✔ CLI-based interactive prompt
✔ Bedrock credentials loaded securely via AWS CLI / environment variables

🧠 How the System Works

The AWS Bedrock Blog Generator project processes blog generation requests using a fully serverless workflow. Below is a step-by-step explanation of how the system works, as shown in the architecture diagram:

1️⃣ User / Postman / Front-End Calls API

A user sends a blog topic (e.g., "Future of AI in Healthcare") through:

Postman

Any HTTP client

Or a front-end application

This request is sent to an Amazon API Gateway endpoint.

2️⃣ Amazon API Gateway

API Gateway receives the HTTP request and acts as a secure entry point to AWS services.
It then forwards the request to an AWS Lambda function.

2️⃣ Amazon API Gateway

API Gateway receives the HTTP request and acts as a secure entry point to AWS services.
It then forwards the request to an AWS Lambda function.

3️⃣ AWS Lambda — Core Blog Generation Logic

The Lambda function performs the main logic:

 Extracts the blog topic from the request body

Lambda saves the generated blog to an S3 bucket as a .txt file, organized by timestamp


