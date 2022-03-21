#  Deploying a Node.js app on AWS 
   main task is to run the nodejs simple application in your machine then deploy it in AWS environment.
   you going to use ECS/EC2 Cluster, Codebuild, ECR, Cloudformation, ALB, EC2 and Cloudwatch services.
   
   1. Deploy Nodjs in your local machine.
         
         - $ mkdir sample-app         
         - $ cd sample-app         
         - $ git clone https://github.com/hubsync/candidate-test-.git
         - $ npm init -y
         - $ npm install express --save
         - $ node server.js
         - 
   2. Create new branch under your name and make sure to upload and merge all files and changes.
   3. Create Dockerfile to dockerize the application and tested in you machine.
   4. create AWS account or use your own existing one.
   5. create ECR and push Docker image you have created in point 3.
   6. create ECS cluster(use EC2 mode) to run the application container.
   7. create task definition to run the application Docker containers in Amazon ECS cluster.
   8. create ECS service to run two instances of the task definition created in point 7, please use the following
      - application load blancer.
      - auto scaling(min=1, max=4, Policy type: Target tracking, ECS service metric: ECSServiceAverageCPUUtilization)          
         
