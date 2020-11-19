# multi-docker-v2
This is an enhancement to multi-docker-v1 repository. In this version we are providing docker integration with Travis-CI and AWS.

Travis-CI will build all production images from our code repo (as described in .travis.yml) file & then publish the images to dockerhub. 
Refer dockerhub link for confirmation as : https://hub.docker.com/

Below is the list of images that will be pushed onto dockerhub : 
 - yourdockerhubid/multi-worker
 - yourdockerhubid/multi-server
 - yourdockerhubid/multi-nginx
 - yourdockerhubid/multi-client
 
Every image mentioned above corresponds to respective docker container. 
Once all the above images are pushed to dockerhub, travis-CI will push the Dockerrun.aws.json file to AWS Elasticbeanstalk.

To run this application successfully on AWS, we need to create Redis & Postgres services separately for interacting with AWS EBS over same security group.(We can keep default VPC which is fine)


- Steps to run the application : 
Under root project directory, run below command : 
  
  docker-compose up --build
  
Above command may take some time to build and deploy all associated images. Once successfully deployed, open the browser and hit URL : http://localhost:3050

Above url shall invoke the Fibonacci Calculator application in React. 

