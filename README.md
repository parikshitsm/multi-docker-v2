# multi-docker-v2
This is an enhancement to multi-docker-v1 repository. In this version we are providing docker integration with Travis-CI and AWS.

Travis-CI will build all production images from our code repo (as described in .travis.yml) file & then publish the images to dockerhub. 
Refer dockerhub link for confirmation as : https://hub.docker.com/

Below is the list of images that will be pushed onto dockerhub : 
 - dockerhubid/multi-worker
 - dockerhubid/multi-server
 - dockerhubid/multi-nginx
 - dockerhubid/multi-client
