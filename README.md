Centos7 Nginx Container
====================================

The Bring Your Own Container deployment pattern provides developers with a generic script they can use to build and deploy containers to the Bluebank Openshift Container Platform. 

Instructions
------------

Clone the BYOC git repository to your workstation
```
git clone https://github.com/sbadakhc/centos7-nginx.git
```

Change directory and execute the script
```
cd centos7-nginx.git
./deploy
```

The script will output some usage examples. Simply copy and paste the working example
```
Usage: ./deploy.sh [option] <arg>

Example: ./deploy.sh -l <label> -p <openshift project> -i <docker image> -t <docker tag> -r <docker registry>
Working example: ./deploy.sh -l xxx -p centos7-nginx-dev -i centos7-nginx -t latest -r registry.example.com:443
```

The command line is as follows. Replace the xxx in the project name with your initials. Retain the hyphons!
```
./deploy.sh -l xxx -p centos7-nginx-dev -i centos7-nginx -t latest -r registry.example.com:443
```

Once the  build and deployment is finished you can browse to your deployment via the Openshift console or by simply browing to https://xxx-centos7-nginx-dev.example.com and remembering to replace the xxx with your the initials you used in the previous command invocation.

--
1
