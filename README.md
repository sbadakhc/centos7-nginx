Centos7 Nginx Container
====================================

The Bring Your Own Container deployment pattern provides developers with a generic script they can use to build and deploy containers to the Openshift Container Platform. 

Instructions
------------

Clone the BYOC git repository to your workstation
```
git clone https://gitlab.bluebank.io/salim.badakhchani/centos7-nginx.git
```

Change directory and execute the script
```
cd centos7-nginx.git
./deploy
```

The script will output some usage examples. Simply copy and paste the working example
```
Usage: ./deploy.sh [option] <arg>

Example: ./deploy.sh -p <openshift project> -i <docker image> -t <docker tag> -r <docker registry>
Working example: ./deploy.sh -p uid-centos7-nginx-env -i centos7-nginx -t latest -r docker-registry-default.bluebank.io:443
```

The command line is as follows. Replace the uid and env in the project name with a unique identifier and the environment respectively . Retain the hyphons!
```
./deploy.sh -l -p uid-centos7-nginx-env -i centos7-nginx -t latest -r docker-registry-default.bluebank.io:443
```

Once the  build and deployment is finished you can browse to your deployment via the Openshift console or by simply browing to https://uid-centos7-nginx-env.bluebank.io and remembering to replace the uid with a unique identifier such as your initals and the env with the corresponding envronment you are building. This is important as project names have to be unique on the platform. 
