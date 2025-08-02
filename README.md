# APIs with Lambda + API Gateway

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-compute-api)

**Author:** Mahdi Ben  
**Email:** hocine.mohamed213@gmail.com

---

![Image](http://learn.nextwork.org/grateful_brown_glamorous_centaur/uploads/aws-compute-api_c9d0e1f2)

---

## Introducing Today's Project!

In this project, I will demonstrate how to build a serverless API using AWS Lambda and Amazon API Gateway. I'm doing this project to learn how to develop and manage backend functionality without provisioning or managing traditional servers.

In this project, I will:

- Develop a serverless Lambda function
- Configure an API using API Gateway
- Connect Lambda with API Gateway to handle requests
- Write clear JSON documentation for the API

Let’s dive in and bring serverless architecture to life.

### Tools and concepts

Services I used were AWS Lambda and Amazon API Gateway. Key concepts I learnt include Lambda functions for serverless computing, API Gateway for managing and deploying APIs, how to connect Lambda to a REST API endpoint, and how to document APIs effectively using JSON.

### Project reflection

This project took me approximately 30 minutes to complete. The most challenging part was connecting the GET method correctly to the Lambda function.

I did this project today to strengthen my understanding of serverless architecture using AWS Lambda and API Gateway. My goal was to learn how to build and deploy an API without managing traditional servers, and this project met that goal. It gave me hands-on experience with key cloud services and helped reinforce concepts like endpoint creation, API methods, and integration with backend functions.

---

## Lambda functions

**AWS Lambda** is a serverless service that runs code in response to events, without needing to manage servers.

I’m using Lambda in this project to **fetch and return user data through an API**, keeping things simple, scalable, and efficient.

The code I added to my function will **query a DynamoDB table for user data based on a `userId`** and return the result. If the `userId` isn’t found, it returns an error. The table and data setup will come in the next project.

![Image](http://learn.nextwork.org/grateful_brown_glamorous_centaur/uploads/aws-compute-api_a1b2c3d5)

---

## API Gateway

APIs are interfaces that let different software systems talk to each other. There are different types of APIs, like REST, SOAP, and GraphQL. My API is a REST API, used to handle HTTP requests and connect users to backend services.

**Amazon API Gateway** is a managed service that lets you create, publish, and manage APIs at any scale.

I'm using API Gateway in this project to **connect users to my Lambda function**, so they can send requests and get responses through a secure, public API endpoint.

When a user makes a request, **API Gateway** sends it to **Lambda**, which runs the code and returns a response. API Gateway then sends that response back to the user, all without managing servers.

![Image](http://learn.nextwork.org/grateful_brown_glamorous_centaur/uploads/aws-compute-api_m3n4o5p6)

---

## API Resources and Methods

API resources are **specific paths or sections** of an API that represent different parts of its functionality. For example, in an app's API, you might have a `/messages` resource for getting messages and a `/users` resource for retrieving user profiles. Each resource handles a specific type of request.

Each resource consists of methods, which are the types of HTTP requests an API can handle, such as GET, POST, PUT, or DELETE. Methods define what action should be taken when a request is made to that specific resource. For example, a GET method retrieves data, while a POST method submits new data.

I created a GET method to retrieve user data from my Lambda function. This allows the API to return information when a client sends a GET request to the users resource.

![Image](http://learn.nextwork.org/grateful_brown_glamorous_centaur/uploads/aws-compute-api_c9d0e1f2)

---

## API Deployment

When you deploy an API, you deploy it to a specific stage. A stage is like a version or environment of your API ; for example, "dev", "test", or "prod". I deployed to the **prod** stage.

To visit my API, I used the **Invoke URL** provided by API Gateway under the deployed **stage (e.g., /prod)**. The API displayed an error because the Lambda function expected a `userId` from the query or the database wasn’t fully set up yet.

![Image](http://learn.nextwork.org/grateful_brown_glamorous_centaur/uploads/aws-compute-api_3ethryj2)

---

## API Documentation

For my project's extension, I am writing API documentation because it helps other developers understand how to interact with my API what endpoints are available, what parameters they need, and what responses to expect. You can do this in API Gateway by adding documentation in JSON format, making your project more professional and easier to use.

Once I prepared my documentation, I published it to a specific stage in API Gateway. You have to publish to a stage because that's how API Gateway knows which version of your API the documentation belongs to.

My published and downloaded documentation showed me the full structure of my API, including the /users resource, the GET method, and metadata like the API title and version. It also included the custom descriptions I wrote, making it clear how the API works and what each part does.

![Image](http://learn.nextwork.org/grateful_brown_glamorous_centaur/uploads/aws-compute-api_z9a0b1c2)

---

---
