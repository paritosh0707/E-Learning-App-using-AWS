# Complete Project Summary along with explanation
## Foundation Models

**Curriculum and Prerequisites**

* **Syllabus:**
    * AWS Bedrock
    * SageMaker
    * AWS services for llms
    * Lambda function
    * API gateways
    * S3
    * EC2
    * Security
* **Prerequisites:**
    * Python basics
    * Foundation of generative AI
    * Optional: knowledge of Length Chain, Lama index, and Vector DB

**Foundational Model**

* Definition: A neural network-based model trained on a massive dataset with a variety of task-specific architectures.
* Types: Homogeneous (text-to-text, image-to-image) and heterogeneous (text-to-image, image-to-text).
* Use cases: Language-related tasks (classification, generation, QA, summarization, chatbots) and vision-related tasks (object detection, segmentation, image generation).
* Training process:
    * Pre-training: Training on a massive dataset with a task-specific architecture (e.g., next word prediction for language models).
    * Fine-tuning: Training on a specific task to improve performance.

**AWS Services for Generative AI**

* **AWS Bedrock:** Provides access to foundational models (llms) such as Lambda 2, Cloud a Model, and the Titan model.
* **AWS SageMaker:** A platform for building, training, and deploying machine learning models, including generative models.
* **Other services:**
    * ECR: Elastic Container Registry for storing and managing container images.
    * API Gateway: For centralizing APIs.
    * Lambda: For creating serverless functions.
    * S3: For storing and managing data.

**Application Development**

The course will guide you through building an e-learning application using the AWS services mentioned above. You will learn how to:

* Access and use foundational models through Bedrock.
* Utilize other AWS services to create a complete infrastructure.
* Fine-tune models and use RAG (Retrial Argument Generation).
* Deploy and implement the application in the cloud.


## AWS Bedrock

**Introduction**

In this video lecture, we will discuss the Amazon Web Services (AWS) Bedrock, a fully managed serverless service for building generative language models (LLMs) applications.

**What is AWS Bedrock?**

AWS Bedrock is a fully managed and serverless service from AWS that simplifies the development and deployment of LLMs applications. Unlike traditional servers, Bedrock takes care of all the configuration and infrastructure management, allowing you to focus on building your application.

**Benefits of Using AWS Bedrock**

* Provides access to a variety of foundation models (FMs) from third-party providers such as Anthropic, Stability AI, Amazon AI, and Lama 2.
* Allows you to make API requests to access these models and generate text, images, or other types of content.
* Offers a user-friendly console for making requests, configuring parameters, and exploring models.
* Provides fine-tuning capabilities to customize models for specific tasks.
* Allows you to provision dedicated capacity for your model deployment, ensuring optimal performance and reliability.

**Architecture of AWS Bedrock**

The Bedrock architecture consists of several components:

* User: The user makes requests to the Bedrock API.
* Bedrock API: The API intermediates between the user and the FMs(Foundation Models).
* Runtime Inferencing and Prompting: The runtime inferencing and prompting components handle the execution of the request and apply any necessary configurations.
* Foundation Models: The FMs are the underlying models that generate the output content. Bedrock provides access to a range of FMs from different providers.
* Custom Models: Bedrock also allows you to build and deploy your own custom models, which can be fine-tuned for specific use cases.
* S3: Amazon Simple Storage Service (S3) can be used to store training data and other resources.

**AWS Bedrock Console Walkthrough**

The Bedrock console provides a user-friendly interface for accessing and managing your models. You can use the console to:

* View available FMs and their capabilities.
* Make API requests and configure inferencing parameters.
* Explore and test models using the built-in playground.
* Fine-tune models to improve their performance for specific tasks.
* Provision dedicated capacity for your model deployment.

**Pricing and Costs of AWS Bedrock**

AWS Bedrock usage is billed based on the following factors:

* **Model Usage:** You are charged based on the number of tokens consumed by your model.
* **Provisioned Capacity:** If you provision dedicated capacity for your model, you will be charged for the capacity you provision, regardless of usage.

It is recommended to estimate your costs using the AWS pricing calculator before deploying your model.

**Conclusion**

AWS Bedrock is a powerful and easy-to-use service for building and deploying LLMs applications. By leveraging Bedrock, you can take advantage of the latest AI advancements and create innovative applications without the need for extensive infrastructure management.

## AWS Lambda Functions

1. **Introduction**
   - Generative AI is a type of AI that can create new data or content from scratch.
   - AWS offers a variety of generative AI services, including Amazon Comprehend, Amazon Rekognition, and Amazon Polly.
   - In this session, we'll focus on using AWS Lambda to create a simple chatbot that uses generative AI.

2. **What is AWS Lambda?**
   - AWS Lambda is a serverless computing service that allows you to run code without having to manage servers.
   - Lambda functions are triggered by events, such as HTTP requests or data changes in S3.
   - Lambda functions can be written in a variety of languages, including Python, Node.js, and Java.

3. **Creating a Lambda function**
   - To create a Lambda function, you can use the AWS Lambda console or the AWS CLI.
   - When creating a Lambda function, you'll need to specify the following:
     - A name for the function
     - The runtime environment for the function
     - The code for the function
     - The IAM role for the function

4. **Using OpenAI with Lambda**
   - To use OpenAI with Lambda, you'll need to create an API key.
   - You can create an API key from the OpenAI website.
   - Once you have an API key, you can use it to authenticate with the OpenAI API.
   - In your Lambda function, you can use the OpenAI API to generate text, translate languages, or answer questions.

5. **Deploying a Lambda function**
   - To deploy a Lambda function, you can use the AWS Lambda console or the AWS CLI.
   - When deploying a Lambda function, you'll need to specify the following:
     - The name of the function
     - The runtime environment for the function
     - The code for the function
     - The IAM role for the function
     - The deployment configuration for the function

6. **Testing a Lambda function**
   - To test a Lambda function, you can use the AWS Lambda console or the AWS CLI.
   - When testing a Lambda function, you can specify the following:
     - The input data for the function
     - The expected output data for the function
   - Lambda will run the function and compare the output data to the expected output data.

7. **Monitoring a Lambda function**
   - To monitor a Lambda function, you can use the AWS Lambda console or the AWS CLI.
   - When monitoring a Lambda function, you can view the following information:
     - The number of times the function has been invoked
     - The duration of each invocation
     - The amount of memory used by each invocation
     - The number of errors that have occurred during each invocation


## Project Architecture || API Gateway

**Introduction**

This session introduces AWS Generative AI and covers the following concepts:

* Using AWS Bedrock knowledge base and AWS service, specifically S3
* How to write Lambda functions
* Connect events and APIs
* Deploy the application from Lambda

**Process**

1. **Create an S3 bucket and upload data**
    * Create an S3 Bucket
    * Upload PDF data
2. **Create a Bedrock knowledge base**
    * Create a new knowledge base
    * Select the S3 bucket as the data source
    * Configure the chunking strategy, embedding model, and vector database

3. **Write a Lambda function**
    * Create a new Lambda function
    * Import the necessary libraries
    * Define the event handler
    * Call the Retrieval and Generation API
    * Return the response
4. **Connect the Lambda function to an API Gateway**
    * Create a new API Gateway
    * Add a new API
    * Configure the API Gateway to call the Lambda function
5. **Deploy the application**
    * Deploy the Lambda function
    * Deploy the API Gateway
6. **Test the application**
    * Send a request to the API Gateway
    * Verify the response

**Architecture Overview**

The following architecture is used for the project:

* User: The user sends a query to the application.
* API Gateway: The API Gateway receives the query and triggers the Lambda function.
* Lambda Function: The Lambda function calls the Retrieval and Generation API to generate a response.
* Retrieval and Generation API: The Retrieval and Generation API interacts with the knowledge base and model to generate a response.
* Knowledge Base: The knowledge base stores the data and metadata used to generate responses.
* Vector Database: The vector database stores the vectors used for embedding the data.

**Creating a Knowledge Base**

1. **Create an S3 Bucket:** Go to the AWS console and create an S3 bucket to store your data.
2. **Upload Data:** Upload the data you want to use to the S3 bucket.
3. **Create a Bedrock Knowledge Base:** Use the AWS Bedrock service to create a knowledge base.
* **Select Data Source:** Choose the S3 bucket where your data is stored.
* **Chunking Strategy:** Select the chunking strategy for your data.
* **Embedding Model:** Select the embedding model to use.
* **Vector Database:** Select the vector database to use.

**Integrating with AWS Services**

1. **Create a Lambda Function:** Create a Lambda function to execute your code.
2. **Connect Lambda to API Gateway:** Connect your Lambda function to the API Gateway to handle incoming requests.
3. **Use Postman to Make Requests:** Use Postman to send requests to the API Gateway and trigger the Lambda function.
4. **Interact with the Knowledge Base:** The Lambda function will interact with the knowledge base using the Retrieval and Generation API.
5. **Configure LLM:** Configure your preferred LLM (language model) to generate responses based on the context provided by the knowledge base.

**Project Implementation**

We will implement these steps in the following sessions:

* **Session 2:** Create S3 Bucket, upload data, and create Bedrock knowledge base.
* **Session 3:** Write Lambda script, configure LLM, and test the application.

**Additional Notes**

* Bedrock knowledge bases require a provision throughput model, which incurs charges.
* Charging is on an hourly basis for model usage and API requests.
* The model loading issue experienced in the demonstration may be a temporary platform issue.