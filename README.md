# Docker_python_api
This Project was created to test out the Python_API_twitter project wihout having to install mongoDB and pyhton modules on local machine.
<br>In order to link the containers, so python could talk to mongoDB, create a network.
<br>docker network create -d bridge --subnet 172.25.0.0/16 apinetwork
<br>
<br>Create the containers assigning then to the network, only assigning the ip to mongo because we binded this IP to it on Dockerfile
<br>docker run --name db -p 27017:27017 --net apinetwork --ip 172.25.0.2 -d mongodb_image
<br>docker run --name web_api -p 2880:2880 --net apinetwork -d python_image
<br>
<br>These images are also available on docker hub
 - kristaum/api_python_twitter:python_api
 - kristaum/mongodb_api:mongodb
