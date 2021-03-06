# DaaS Docker container
## /dev/null as a service

Built with latest Debian and Nginx, and version 1.0 of DaaS

## Installation
Use docker to build the container and then run it on port 80.

```
git clone https://github.com/boardstretcher/docker-files.git
cd docker-files/devnull-1.0_debian
docker build -t devnull .
docker run -p 80:80 -d devnull
```

You may then test with a curl command that your information is being dropped by dev/null

```
touch this
curl -v -d @this -X POST http://your-ip-address/dev/null
```

## About

From: http://devnull-as-a-service.com/
> In modern days everything is a service. You create documents, upload photos, deploy computers, but what's happening to your trash? That's why we're launching /dev/null to the cloud.
>
> IAAS, SAAS, PAAS, holy fuckshit, we call our baby DAAS.
>
> Don't get rid of your data yourself anymore. Use our distributed service located in over 380 countries! No matter if you're using it personally or for your business: plans for whole companies are available as well.
>
> Just because, of course, everything should be a managed-service somewhere in the internet!
