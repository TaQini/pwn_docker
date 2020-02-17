# Pwn Docker

> A docker repository for deploying CTF challenges on CTFd with CTFd-whale

## Build docker image

```shell
$ ./deploy.py your_pwn_challenge docker_REPOSITORY_name
```

> your_pwn_challenge: binary file of your pwn challenge 
>
> docker_REPOSITORY_name: image name of docker (in lower case)

## Deploy to CTFd

install CTFd-whale first: [CTFd-Whale 推荐部署实践](https://www.zhaoj.in/read-6333.html)

add a Dynamic docker challenge with following configure:

> Docker Image: docker_REPOSITORY_name
> 
> Frp Redirect Type: Direct
> 
> Frp Redirect Port: 9999

