We created a simple web application deployed using AWS serverless architecture, leveraging Amazon Lambda, DynamoDB, API Gateway, and Identity and Access Management (IAM) for secure and efficient functionality. This application is designed to handle user requests through AWS Lambda functions, which serve as the backend logic. Data is stored in Amazon DynamoDB, ensuring fast and scalable access. Amazon API Gateway facilitates communication between the front end and backend, while IAM ensures secure access control and permissions management across services. This architecture provides a fully managed, highly available solution that scales with user demand and minimizes operational overhead.


Setting Up AWS Lambda Functions Create Lambda Functions: Navigate to the AWS Lambda Console within the AWS Management Console. Click on "Create function" and set up new functions for handling POST, GET  using the provided lambdafuction.py.  Assign appropriate roles to these Lambda functions, ensuring they have access to interact with DynamoDB.

Configuring API Gateway Create a New API: Go to the API Gateway Console and create a new REST API. Set up resources and methods (GET, POST) corresponding to your Lambda functions. Ensure that each method is correctly linked to its corresponding Lambda function. Enable CORS: For each method, enable CORS to allow your web application to interact with these endpoints. You can enable CORS by selecting the method, clicking on "Actions", and selecting "Enable CORS".


Creating a DynamoDB Table Set Up DynamoDB Table: Go to the DynamoDB Console and create a new table, e.g., form. Define the primary key as 'id'.
Configuring IAM Role for Lambda Assign IAM Role: In the IAM Console, ensure that the execution role assigned to your Lambda functions has the necessary permissions to access DynamoDB.


In conclusion, this setup leverages AWS's serverless services to create a scalable and secure web application. By configuring Lambda functions with appropriate roles, integrating them with API Gateway and establishing a DynamoDB table for data storage, we ensure an efficient and reliable architecture. This setup minimizes infrastructure management while providing a robust backend solution capable of handling HTTP requests securely. With the correct IAM permissions, each component works seamlessly together, offering a cost-effective, highly available, and flexible environment to support our application’s requirements.
