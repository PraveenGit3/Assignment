# Assignment

 
 
 ## Question-1: Dockerise and deploy hello-world.jar (in the GitHub repository associated with this challenge) to Amazon Web Services using their Elastic Container Service. This application contains a simple API with Open API documentation, and should be deployed in a secure isolated environment with only HTTPS exposed to the world.

 ### Sol:
 
 1.Provisoned AWS ec2 instances 
 
 2.created dockerfile locally and deployed to aws ec2 isntances 
 
 3.Built the docker file and ran container to expose the Web APP on port 3000
 
 4.Now pushed our docker file to AWS ECR service
 
 5.Created AWS ECS cluster with leveraging ECR and Fartgate(Task ,ALB and services)
 
 6.Exposed the WEBAPP on Isolated environment 
 
 Ssome of the commands utilised in creation and build of docker containers

#docker build -f Dockerfile -t hello-world.jar:latest .

#docker run  -p 3000:80  hello-world.jar:1.0.latest

#### Findings

1.ECS is a fully managed platform from AWS which eliminates all the infrastructure  dependencies which we deal in  non cloud Container orchestration  platforms and highly secure and cost efficient  and some of the principles I adhered here are  infrastructure as code  and being caution to failure  eliminating  or anticipating downtimes  to achieve high availability

2.If there is no of running multiple instances of container is required we could use docker compose   by following commands 

docker-compose up --scale app=2

3.If I need to expose application to external databases It is best practise to expose them on 3306 port 

4.This objective can well engineered if we can structure our  application and infrastructure creations using Infra structure as code and  following devops principles like   utilising CI/CD pipeline and  SCM based technologies like Github  as source of truth for all code  and platform changes. 

**Align center:**
<p align="center" width="100%">
    <img width="93%" src="https://github.com/PraveenGit3/Assignment/blob/main/Screenshot%202023-02-02%20at%2021.18.44.png">
</p>
 

 # Code files are saved in subdirectories 1 & 2
 
 ## Question-2:create a CodePipeline to deploy the application and infrastructure created.
 
 ### Sol:
 
  1. Create a pipeline in Jenkins2.Write a jenkins file using DSL grrovy i.e, Pipeline as Code

  2.Build  and run the pipeline and validate your files in Aws ECS
 
  3.Provision all the infrastructure architected from 1st objective via terraform on AWS platform  and  entire terraform code bases was structured in different files  to maintain  clean code  visibiity and better understanding
  
  #### Findings
  
  1.Automated releases , Efficient   deployments,  code reconfigurations   by leveraging Jenkins pipeline  and utilised pipeline as code philosophy for Continuous integration and continuous deployment tasks using bash scripting for docker orchestration 

2.One of the reasons which I strongly believe this could be good practices are Code reconfiguration for example any change request will initiated only through change in Github repos eliminating discrepancy in deployments and reducing manual build process.

3.Some of my recommendation could include bring CI/CD practices in creating of Platform  for applications  just like application lifecycle , Usage of Secure service for authentication like AWS-KMS ,SCM polling ,etc

**Align center:**
<p align="center" width="100%">
    <img width="93%" src="https://github.com/PraveenGit3/Assignment/blob/main/Screenshot%202023-02-02%20at%2021.31.37.png">
</p>
