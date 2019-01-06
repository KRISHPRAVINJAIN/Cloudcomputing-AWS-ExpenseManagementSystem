# ExpenseManagementSystemCloudcomputing

• Designed and built fault tolerant web application using node js hosted on cloud computing platform (Amazon Web Services) using IaaS, PaaS & SaaS services such as EC2, EBS, Route53, SES, ELB, CloudWatch, IAM, RDS, Lambda, NoSQL (DynamoDB) and S3 object store
• Implemented Continuous Delivery using GitHub, Travis CI and Amazon Code-Deploy
• The web application allows users to create, update, delete and maintain the history of their transactions

To Run Scripts for AWS Cloud formation:

 # Infrastructure as a Code:
 This readme.md contains steps to build your AWS cloud infrastrcture using AWS CLI
 
 ## Getting Started:
 For this, we will be programming VPC i.e Virtual Private Cloud using AWS cloudformation.
 
 ## Prerequisites:
 1. VMware Work Station OR
 2. Oracle Virtual BOx
 3. Fedora
 4. Pip
 5. AWS CLI
 
```
sudo apt-get install python-pip
```
 
 ## For AWS:
 First make sure that you have installed AWS CLI in your fedora
 ```
 $ pip install awscli --upgrade --user
 ```
 
 Now, we will configure our AWS. Make sure you configure your AWS with your Access Key and Secret Key. In order to set-up the AWS infrastrucutre, use 
 the following command
 
```
 $aws configure
```

## Running Scripts:
Before running the scripts, it is important to make a note that all the scripts, template file should be in the same folder.

To create and configure required networking resources using AWS CloudFormation:
```
> ./csye6225-aws-cf-create-stack.sh
```
To delete  Cloudformation Stack:
```
> ./csye6225-aws-cf-terminate-stack.sh
```
 
## Running application stack scripts:

To create application stack:
```
> ./csye6225-aws-cf-create-application-stack.sh  [STACK_NAME]
```

To Delete application stack:
```
> ./csye6225-aws-cf-terminate-application-stack.sh [STACK_NAME]
```
##Running cicd stack script:
To create cicd
```
> ./csye6225-aws-cf-create-cicd.sh [STACK_NAME]
```
To delete cicd
```
> ./csye6225-aws-cf-terminate-cicd-stack.sh [STACK NAME]
```
##Running autoscaling stack scripts:
To create autoscaling
```
> ./csye6225-aws-cf-create-autoscaling-stack.sh [STACK_NAME]
```
To delete cicd
```
> ./csye6225-aws-cf-terminate-autoscaling-stack.sh [STACK NAME]
```
##Running Serverless stack scripts:
To create serverless
```
> ./csye6225-aws-cf-create-serverless-stack.sh [STACK_NAME]
```
To delete cicd
```
> ./csye6225-aws-cf-terminate-serverless-stack.sh [STACK NAME]
```
##Running WAF RESOURCE stack script:
To create waf resource
```
> ./csye6225-aws-cf-create-WAFResource.sh [STACK_NAME]
```
To delete cicd
```
> ./csye6225-aws-cf-terminate-WAFResource.sh [STACK NAME]
```

To Run Web Application:

 # Web Application for CRUD Operations using AUTHENTICATION and AUTHORRIZATION:
 This readme.md contains steps to start and run your Web Application for CRUD Operations using AUTHENTICATION and AUTHORIZATION
 
 ## Getting Started:
 For this, we will be installing NODE Js and its dependencies
 
 ## Prerequisites:
 1. VMware Work Station OR
 2. VMware Fusion(Mac) OR
 3. Oracle Virtual Box
 4. Fedora
 5. mySQL
 6. Node Js Version 8.12.0
 
 ## Installing Node Js
Install Node JS Version 8.12.0 from the following site: https://nodejs.org/en/download/ or from terminal run below command in the terminal
```
sudo dnf install nodejs
```
 
 ## For dependencies:
 Install all required node dependencies using below command in the terminal
```
npm install
```
## Starting you project:
Once all dependencies are installed, start your project using following command in the terminal
```
node app.js 
```
The server will start running on port 5000
Open your browser, type localhost:3000 and start

## Perform Operations
Open Postman application to perform CRUD operations on transaction

## To Set up configurations
The config.js file has to be made in you webapp folder and must contain all configurations like belo
```
var config = {
    Dev: {
        name: "dev",
        aws: {
            accessKeyId: "youraccesskey",
            secretAccessKey:"yoursceretaccesskey"
        },
        database: {
            host: 'databasehost',
            user: 'username',
            password: 'password',
            db_name: 'databasename'
        }
    },
    default: {
        name: "default",
        database: {
            host: 'databasehost',
            user: 'username',
            password: 'password',
            db_name: 'dataasename'
        },
        
    },
}

exports.get = function get(env) {
    return config[env] || config.default;
}
```
##TO RUN THE APPLICATION ON CLOUD EC2 INSTANCE
DEPLOY THE APPLICATION USING TRAVIS CI



