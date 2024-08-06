# Ejercicio 1
## Docker pull ubuntu
* Using default tag: latest 
* latest: Pulling from library/ubuntu
* 9c704ecd0c69: Pull complete 
* Digest: sha256:2e863c44b718727c860746568e1d54afd13b2fa71b160f5cd9058fc436217b30
* Status: Downloaded newer image for ubuntu:latest
* docker.io/library/ubuntu:latest 

## docker pull python:3.9
* 3.9: Pulling from library/python
* ca4e5d672725: Pull complete 
* 30b93c12a9c9: Pull complete 
* 10d643a5fa82: Pull complete 
* d6dc1019d793: Pull complete 
* c387064957b7: Pull complete 
* 26766ebde481: Pull complete 
* 8a42d17fd0e2: Pull complete 
* 79eda865cc8a: Pull complete 
* Digest: sha256:fea84f3a3b72c41efe7fc3b07ae209c6856b852b942c05fa88b747b74f70e711
* Status: Downloaded newer image for python:3.9
* docker.io/library/python:3.9

# Ejericio 2
## docker run -it ubuntu bash 
* root@217a83fae32b:/# 

## docker run -d -p 8080:80 httpd
* Unable to find image 'httpd:latest' locally
* latest: Pulling from library/httpd
* efc2b5ad9eec: Already exists 
* fce1785eb819: Pull complete 
* 4f4fb700ef54: Pull complete 
* f214daa0692f: Pull complete 
* 05383fd8b2b3: Pull complete 
* 88ad12232aa1: Pull complete 
* Digest: sha256:932ac36fabe1d2103ed3edbe66224ed2afe0041b317bcdb6f5d9be63594f0030
* Status: Downloaded newer image for httpd:latest
* 16d7939d022282e17124461c1ceb2b48d70c0dad1e4cc497e142688069b14cab

# Ejercicio 3
## docker rm 217a83fae32b
* 217a83fae32b
## docker container prune
* WARNING! This will remove all stopped containers.
* Are you sure you want to continue? [y/N] y
* Total reclaimed space: 0B

# Laboratorio 2

## TEMA 1
### Ejercicio 1
#### docker build -t ubuntu-updated:latest .
* [+] Building 9.2s (6/6)FINISHED                                                                                         docker:default
 => [internal] load build definition from dockerfile                                                                               0.2s
 => => transferring dockerfile: 97B                                                                                                0.0s
 => [internal] load metadata for docker.io/library/ubuntu:latest                                                                   0.0s
 => [internal] load .dockerignore                                                                                                  0.1s
 => => transferring context: 2B                                                                                                    0.0s
 => [1/2] FROM docker.io/library/ubuntu:latest                                                                                     0.1s
 => [2/2] RUN apt-get update && apt-get upgrade -y                                                                                 7.7s
 => exporting to image                                                                                                             0.7s 
 => => exporting layers                                                                                                            0.5s 
 => => writing image sha256:33ff0081d2a0cd6dd2ca830073799d64a9410779595f5280bddefdd3b57d897e                                       0.0s 
 => => naming to docker.io/library/ubuntu-updated:lates

### Ejercicio 3
#### docker build -t ubuntu-updated:latest .
* [+] Building 13.3s (6/6) FINISHED                                                                                        docker:default
 => [internal] load build definition from dockerfile                                                                               0.0s
 => => transferring dockerfile: 138B                                                                                               0.0s
 => [internal] load metadata for docker.io/library/ubuntu:latest                                                                   0.0s
 => [internal] load .dockerignore                                                                                                  0.1s
 => => transferring context: 2B                                                                                                    0.0s
 => CACHED [1/2] FROM docker.io/library/ubuntu:latest                                                                              0.0s
 => [2/2] RUN apt-get update && apt-get install -y nginx                                                                          12.1s
 => exporting to image                                                                                                             0.8s 
 => => exporting layers                                                                                                            0.7s 
 => => writing image sha256:ad3ac71160328144d55352bc299a5db4ef40b55a5f6e171626392c61c64aa282                                       0.0s 
 => => naming to docker.io/library/ubuntu-updated:latest 

### Ejercicio 4 
#### docker build -t my-nginx:latest .
* [+] Building 0.4s (6/6)                       FINISHED                                                                                         docker:default
 => [internal] load build definition from dockerfile                                                                               0.0s
 => => transferring dockerfile: 138B                                                                                               0.0s
 => [internal] load metadata for docker.io/library/ubuntu:latest                                                                   0.0s
 => [internal] load .dockerignore                                                                                                  0.0s
 => => transferring context: 2B                                                                                                    0.0s
 => [1/2] FROM docker.io/library/ubuntu:latest                                                                                     0.0s
 => CACHED [2/2] RUN apt-get update && apt-get install -y nginx                                                                    0.0s
 => exporting to image                                                                                                             0.1s
 => => exporting layers                                                                                                            0.0s
 => => writing image sha256:ad3ac71160328144d55352bc299a5db4ef40b55a5f6e171626392c61c64aa282                                       0.0s
 => => naming to docker.io/library/my-nginx:latest   

#### docker run -d -p 80:80 my-nginx:latest
* bcdb15b298aeba512f4da6e09f6622936ef3ff52f18478b827d3c3279ed30445

### Ejercicio 5
#### docker build -t my-nginx:latest .
* [+] Building 0.6s (6/6) FINISHED                                                                                         docker:default
 => [internal] load build definition from dockerfile                                                                               0.0s
 => => transferring dockerfile: 148B                                                                                               0.0s
 => [internal] load metadata for docker.io/library/ubuntu:latest                                                                   0.0s
 => [internal] load .dockerignore                                                                                                  0.0s
 => => transferring context: 2B                                                                                                    0.0s
 => [1/2] FROM docker.io/library/ubuntu:latest                                                                                     0.0s
 => CACHED [2/2] RUN apt-get update && apt-get install -y nginx                                                                    0.0s
 => exporting to image                                                                                                             0.1s
 => => exporting layers                                                                                                            0.0s
 => => writing image sha256:a7f7cd8be481bb875075d135e0d6ca0aa05ef4c596b35ca710514b93e384a69c                                       0.0s
 => => naming to docker.io/library/my-nginx:latest 

