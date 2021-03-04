# Serverless Spring Boot 2 with container image example
This projce uses Spring Boot Pet Store project from awslab as a foundation as it has all the setting to run Spring Boot application on Lambda. Find out more -> (https://github.com/awslabs/aws-serverless-java-container)
## Pre-requisites
* [AWS CLI](https://aws.amazon.com/cli/)
* [SAM CLI](https://github.com/awslabs/aws-sam-cli)
* [Gradle](https://gradle.org/)

## Test the project locally 
Open a terminal of your choice, and navigate to the root of the project where the template.yaml is. Then run...
```
$ sam build -u
```

This command compiles the application and prepares a deployment package in the `.aws-sam` sub-directory.

To test the application locally, run the following command after the build is success.

```
sam local start-api
```

Now the service will run on http://localhost:3000/ 
You can test it by calling GET: http://localhost:3000/pets 

```
curl http://localhost:3000/pets
```

The application will take sometimes before returning anything, because Spring Boot is initialising....

To deploy the application in your AWS account, you can use the SAM CLI's guided deployment process and follow the instructions on the screen

```
$ sam deploy --guided
```
