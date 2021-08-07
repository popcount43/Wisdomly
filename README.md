
Nowadays, Online Book Stores are gaining enormous popularity.In this project we have created an Online BookStore using React,AWS Amplify.The project further aims to give a checkout and payment option using Stripe.

The project is mainly divided into two parts :
<ol>
<li>Creating the Resources on AWS. (E.g. DynamoDB Database, AppSync API, S3 Image Storage, Lambda Serverless Functions, etc.)
<li>Consuming those Resources from the Online Book Store Frontend React Application.

<li>Online Book Store frontend is a React application that is hosted in an S3 bucket (A). The bucket has static web hosting enabled so that it can serve the website over the internet.</br>
<li>All the book images are stored in another S3 bucket (B) with public access so that both authenticated and unauthenticated users can view book images.</br>
<li>The React application communicates with the AWS backend resources securely via AWS Amplify JavaScript Library (C).</br>
<li>Authentication and Authorization are handled by Amazon Cognito (D) that provides a scalable user directory with user authentication flows.</br>
<li>The book store has a GraphQL API powered by AWS AppSync (E). The React application uses the Amplify library to handle all the CRUD (Create, Read, Delete, Update) operations by issuing Queries and Mutations to the AppSync API.</br>
<li>The AppSync API is connected with two data sources — Amazon DynamoDB and Lambda. The Lambda data source will be used when a customer has placed a book order. The DynamoDB data source is used for the rest of the queries and mutations.</br>
<li>The AppSync API will use VTL (Velocity Template Language) scripts (G) to manipulate data in the DynamoDB (F). AWS Amplify Library automatically generates these VTL scripts.</br>
<li>When a customer has placed an order, AppSync invokes the “Make Payment” lambda function(H). It will attempt to charge the customer using Stripe. If the payment has been successful, AppSync will invoke the “Create Order” lambda function(I) to create the order in the database.</br>
</ol>
<h3>In this architecture, the AWS Amplify plays a significant role.</h3>

<h2>The Architecture Looks as follows:</h2>
![design](https://user-images.githubusercontent.com/86571685/128613898-5b6210f0-699d-40a0-a5ae-acede5b598be.png)

<h2>The Estimated Budget per month assuming the services run with maximum consistency is as follows : </h2>
[Budget.xlsx](https://github.com/popcount43/Wisdomly/files/6949840/Budget.xlsx)
![Screenshot (59)](https://user-images.githubusercontent.com/86571685/128614351-c5723432-c223-46dd-adf0-fda56fea7479.png)

<h1>The front end looks as follows : </h1>


![Screenshot (54)](https://user-images.githubusercontent.com/86571685/128614375-9ffbab95-61a7-4827-bcd2-7b4f6820f932.png)
![Screenshot (55)](https://user-images.githubusercontent.com/86571685/128614400-91191513-b5ab-451d-ad9b-bba12049a1e5.png)
![Screenshot (56)](https://user-images.githubusercontent.com/86571685/128614401-f6634965-f091-48a8-a7b2-7ff35b433906.png)








