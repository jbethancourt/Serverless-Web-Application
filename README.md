# Serverless-Web-Application
with AWS Lambda, Amazon API Gateway, AWS Amplify, Amazon DynamoDB, and Amazon Cognito

# Overview
In this tutorial, you will create a serverless web application that enables users to request unicorn rides from the Wild Rydes fleet. The application will present users with an HTML-based user interface for indicating a pick-up location and a RESTful web service on the backend to submit the request for dispatching a unicorn. The application will also provide facilities for users to register with the service and log in before requesting rides.
Prerequisites
To complete this tutorial, you will need an AWS account, AWS CLI installed, an account with ArcGIS to add mapping to your app, a text editor, and a web browser. If you don't already have an AWS account, you can follow the Setting Up Your AWS Environment getting started guide for a quick overview.

# Application Architecture
The application architecture uses AWS Lambda, Amazon API Gateway, Amazon DynamoDB, Amazon Cognito, and AWS Amplify Console. Amplify Console provides continuous deployment and hosting of the static web resources including HTML, CSS, JavaScript, and image files which are loaded in the user's browser. JavaScript executed in the browser sends and receives data from a public backend API built using Lambda and API Gateway. Amazon Cognito provides user management and authentication functions to secure the backend API. Finally, DynamoDB provides a persistence layer where data can be stored by the API's Lambda function.

![Application Architecture](./images/Serverless_Architecture.png)

### Static Web Hosting

AWS Amplify hosts static web resources including HTML, CSS, JavaScript, and image files which are loaded in the user's browser.

### User Management

Amazon Cognito provides user management and authentication functions to secure the backend API.

### Serverless Backend

Amazon DynamoDB provides a persistence layer where data can be stored by the API's Lambda function.

### RESTful API

JavaScript executed in the browser sends and receives data from a public backend API built using Lambda and API Gateway.

# Modules
This tutorial is divided into five modules. Each module describes a scenario of what we're going to build and step-by-step directions to help you implement the architecture and verify your work. 

1. Host a Static Website (15 minutes): Configure AWS Amplify to host the static resources for your web application with continuous deployment built in
2. Manage Users (30 minutes): Create an Amazon Cognito user pool to manage your users' accounts
3. Build a Serverless Backend (30 minutes): Build a backend process for handling requests for your web application
4. Deploy a RESTful API (15 minutes): Use Amazon API Gateway to expose the Lambda function you built in the previous module as a RESTful API
5. Terminate Resources (10 minutes): Terminate all the resources you created throughout this tutorial
