#  Deploying a Node.js app on AWS 
   the task is to automate the nodejs application deployment in AWS environment using Cloudformation and Codebuild.
   you may use ECS/EC2 Cluster, Codebuild, ECR, Cloudformation, ALB, EC2, Cloudwatch and other services.  
   
   1. Deploy Nodjs in your local machine.         

         - $ git clone https://github.com/hubsync/candidate-test.git
         - $ cd candidate-test
         - $ npm init -y
         - $ npm install express --save
         - $ node server.js
          
   2. Create new branch under your name and make sure to upload and merge all files and changes.
   3. Create Dockerfile to dockerize the application and test it in your machine.(listen to port 3000)
   4. create AWS account or use your own existing one.
   5. create ECR and push Docker image you created in step 3.
   6. create ECS cluster(use EC2 mode) to run the application container, create launch configuration and ASG (min. capacity:1, max. capacity:5, desired capacity: 2,  no scalling policy required)
   7. create task definition to run the application Docker containers in Amazon ECS cluster. enable cloudwatch logs.
   8. create ECS service to run two instances of the task definition created in step 7, in addition please add the following
      - application load blancer.
      - auto scaling(min=1, max=4, Policy type: Target tracking, ECS service metric: ECSServiceAverageCPUUtilization)
   9. once you done and verify application response using ALB endpoint, create cloudfromation template to automate steps 6, 7 and 8 then merge it in your GitHub branch for review.
   10. use AWS codebuild to automate steps 3 and 5.          
         
