# Assignment

 ## Question-1: Dockerise and deploy hello-world.jar (in the GitHub repository associated with this challenge) to Amazon Web Services using their Elastic Container Service. This application contains a simple API with Open API documentation, and should be deployed in a secure isolated environment with only HTTPS exposed to the world.

 ### Sol:
 
 1.Provisoned AWS ec2 instances 
 
 2.created dockerfile locally and deployed to aws ec2 isntances 
 
 3.Built the docker file and ran container to expose the Web APP on port 3000
 
 4.Now pushed our docker file to AWS ECR service
 
 5.Created AWS ECS cluster with leveraging ECR and Fartgate(Task ,ALB and services)
 
 6.Exposed the WEBAPP on Isolated environment 

 
 
 
 ## Question-2:create a CodePipeline to deploy the application and infrastructure created.
 
 ### Sol:
 
  1. Create a pipeline in Jenkins2.Write a jenkins file using DSL grrovy i.e, Pipeline as Code

  2.Build  and run the pipeline and validate your files in Aws ECS
 
  3.Access the webapp
