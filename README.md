# Pwn Docker

> 通过CTFd-whale插件在CTFd平台快速部署pwn题目

## 生成docker镜像

```shell
$ ./deploy.py your_pwn_challenge docker_REPOSITORY_name
```

> your_pwn_challenge: ELF类型的题目文件 
> docker_REPOSITORY_name: Docker镜像名(只允许小写)

举个栗子：
 - 题目位置：/home/TaQini/pwn/hellopwn
 - 镜像名：hellopwn
 - 一键生成镜像：
    ```shell
    $ ./deploy.py /home/TaQini/pwn/hellopwn hellopwn
    ```
## 部署到CTFd平台

CTFd-whale插件安装教程：[CTFd-Whale 推荐部署实践](https://www.zhaoj.in/read-6333.html)

新建题目，选择题目类型为`dynamic_docker `，并进行如下配置：

> Docker Image: 刚刚生成的镜像名
> Frp Redirect Type: Direct
> Frp Redirect Port: 9999