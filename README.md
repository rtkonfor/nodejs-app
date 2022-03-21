#  Deploying a Node.js app on AWS 
   main task is to run the nodejs simple application in your machine then deploy it in AWS environment.
   you going to use ECS/EC2 Cluster, Codebuild, ECR, Cloudformation, ALB, EC2 and Cloudwatch services.
   
   1. Deploy Nodjs in your local machine.
         // create a new directory
         $ mkdir sample-app         
         // change to new directory
         $ cd sample-app
         // clone the repo.
         $ git clone https://github.com/hubsync/candidate-test-.git
         // Initialize npm
         $ npm init -y
         // install express
         $ npm install express --save
         // run a server.js file
         $ node server.js
         
