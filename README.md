# Serverless-Web-Application
with AWS Lambda, Amazon API Gateway, AWS Amplify, Amazon DynamoDB, and Amazon Cognito

Overview
In this tutorial, you will create a serverless web application that enables users to request unicorn rides from the Wild Rydes fleet. The application will present users with an HTML-based user interface for indicating a pick-up location and a RESTful web service on the backend to submit the request for dispatching a unicorn. The application will also provide facilities for users to register with the service and log in before requesting rides.
Prerequisites
To complete this tutorial, you will need an AWS account, AWS CLI installed, an account with ArcGIS to add mapping to your app, a text editor, and a web browser. If you don't already have an AWS account, you can follow the Setting Up Your AWS Environment getting started guide for a quick overview.

Application Architecture
The application architecture uses AWS Lambda, Amazon API Gateway, Amazon DynamoDB, Amazon Cognito, and AWS Amplify Console. Amplify Console provides continuous deployment and hosting of the static web resources including HTML, CSS, JavaScript, and image files which are loaded in the user's browser. JavaScript executed in the browser sends and receives data from a public backend API built using Lambda and API Gateway. Amazon Cognito provides user management and authentication functions to secure the backend API. Finally, DynamoDB provides a persistence layer where data can be stored by the API's Lambda function.

![Application Architecture](./images/Serverless_Architecture.png)

Static Web Hosting

AWS Amplify hosts static web resources including HTML, CSS, JavaScript, and image files which are loaded in the user's browser.

User Management

Amazon Cognito provides user management and authentication functions to secure the backend API.

Serverless Backend

Amazon DynamoDB provides a persistence layer where data can be stored by the API's Lambda function.

RESTful API

JavaScript executed in the browser sends and receives data from a public backend API built using Lambda and API Gateway.
