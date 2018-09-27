# MongoDB Image
This Dockerfile contains the configuration to have a mongoDB running on a debian machine
<br>You will need to note a couple of things:
 - GPG Key, the instructions to generate it can be found on mongoDB site, section: Install MongoDB --> Verify Integrity of MongoDB Packages
 - Define proper version to be installed on MONGO_MAJOR and MONGO_VERSION env variables.
 - I have binded IP 172.25.0.2 on start so the python code could have connection to mongoDB.
