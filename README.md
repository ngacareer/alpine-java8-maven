## Quick reference
- Created by: <a href="https://github.com/ngacareer">ngacareer</a>
- Where to get help: <a href="https://forums.docker.com/">the Docker Community Forums</a>, <a href="https://dockr.ly/slack">the Docker Community Slack</a>, or <a href="https://stackoverflow.com/search?tab=newest&amp;q=docker">Stack Overflow</a>

## Supported tags and respective Dockerfile links
- <a href="https://github.com/ngacareer/alpine-java8-maven/blob/main/Dockerfile">latest (3.6.3)</a>

## Quick reference (cont.)
- Where to file issues <a href="https://github.com/ngacareer/alpine-java8-maven/issues">https://github.com/ngacareer/alpine-java8-maven/issues</a>

## What is Maven?

<a href="http://maven.apache.org/">Apache Maven</a> is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.

## What is alpine-maven ? 

Linux lightweight, It has been integrated jdk 1.8 and maven

## How to use this image
- On Docker 
```
docker run -itd --name alpine-java8-maven ngacareer/alpine-java8-maven
docker exec -it alpine-java8-maven bin/sh
# mvn --version
 ```
- On Kubernetes
 ```
kubectl run alpine-java8-maven --image=ngacareer/alpine-java8-maven
kubectl exec -it pod/alpine-java8-maven bin/sh
# mvn --version
 ```
- On OpenShift
 ```
oc new-app --docker-image=ngacareer/alpine-java8-maven --name=alpine-java8-maven
oc exec -ti $(oc get pod -l app=alpine-java8-maven -o jsonpath="{.items[0].metadata.name}") bin/sh
$ mvn --version
 ```
## License

Copyright © 2021 Ngacareer

All contents licensed under the [MIT License](LICENSE)
