# CODYSSEY
# AI/SW 개발 워크스테이션 구축하기

## 1. 프로젝트 개요
AI/SW 개발 워크스테이션 구축하기


### 미션 목표 요약
- [x] 목표 1: 터미널 기반 파일/디렉토리 조작 및 권한 이해
- [x] 목표 2: Docker를 활용한 컨테이너 실행 및 관리
- [x] 목표 3: 포트 매핑 및 마운트를 통한 외부 연결 및 데이터 관리 이해
- [x] 목표 4: Git/GitHub를 통한 버전 관리 및 협업 환경 구성


---

## 2. 실행 환경

| 항목 | 버전/정보 |
|------|---------|
| OS | macOS 15.7.4 |
| 쉘 | zsh |
| Docker | 28.5.2 |
| Git | 2.53.0 |
| 언어 | Python 3.12.13 |

---

## 3. 수행 항목 체크리스트

### 터미널/권한
- [x] 터미널 접근 권한 확인
- [x] 파일/디렉토리 생성 및 삭제
- [x] 권한 변경 실습

### Docker
- [x] Docker 설치 및 실행 확인
- [x] `docker --version` 확인 완료

### Dockerfile
- [x] Dockerfile 작성 완료
- [x] 이미지 빌드 성공
- [x] `docker build -t 이미지명 .` 실행 완료

### 포트/볼륨
- [x] 포트 매핑 설정: `8080:80, 8081:80`
- [x] 볼륨 마운트 설정: `/app:/data`
- [x] 컨테이너 실행 성공

### Git/GitHub
- [x] 로컬 저장소 초기화
- [x] 원격 저장소 연결
- [x] 커밋 및 푸시 완료

---

## 4. 검증 방법 및 결과


### 4.1 터미널 기본 조작
**명령어 : ls -la**

* total 15
drwxr-x---+ 20 beep_beep2643  beep_beep2643   640 Apr  2 19:19 .
drwxr-xr-x   7 root           admin           224 Apr  2 19:03 ..
-r--------   1 beep_beep2643  beep_beep2643     7 Apr  2 19:03 .CFUserTextEncoding
drwx------+  2 beep_beep2643  beep_beep2643    64 Apr  2 19:04 .Trash
drwxr-xr-x   5 beep_beep2643  beep_beep2643   160 Apr  2 19:04 .docker
drwxr-xr-x  10 beep_beep2643  beep_beep2643   320 Apr  2 19:04 .orbstack
drwxr-xr-x   3 beep_beep2643  beep_beep2643    96 Apr  2 19:04 .ssh
drwxr-xr-x   3 beep_beep2643  beep_beep2643    96 Apr  2 19:04 .vscode
-rw-------   1 beep_beep2643  beep_beep2643    17 Apr  2 19:16 .zsh_history
drwx------   7 beep_beep2643  beep_beep2643   224 Apr  2 19:19 .zsh_sessions
drwx------+  3 beep_beep2643  beep_beep2643    96 Apr  2 19:03 Desktop
drwx------+  3 beep_beep2643  beep_beep2643    96 Apr  2 19:03 Documents
drwx------+  4 beep_beep2643  beep_beep2643   128 Apr  2 19:10 Downloads
drwx------@ 78 beep_beep2643  beep_beep2643  2496 Apr  2 19:30 Library
drwx------   3 beep_beep2643  beep_beep2643    96 Apr  2 19:03 Movies
drwx------+  3 beep_beep2643  beep_beep2643    96 Apr  2 19:03 Music
drwx------   4 beep_beep2643  beep_beep2643   160 Apr  2 19:04 OrbStack
drwx------+  4 beep_beep2643  beep_beep2643   128 Apr  2 19:03 Pictures
drwxr-xr-x+  4 beep_beep2643  beep_beep2643   128 Apr  2 19:03 Public


**명령어 : mkdir test-dir**

* total 16
drwxr-x---+ 20 beep_beep2643  beep_beep2643   640 Apr  2 19:46 .
drwxr-xr-x   7 root           admin           224 Apr  2 19:03 ..
-r--------   1 beep_beep2643  beep_beep2643     7 Apr  2 19:03 .CFUserTextEncoding
drwx------+  2 beep_beep2643  beep_beep2643    64 Apr  2 19:04 .Trash
drwxr-xr-x   5 beep_beep2643  beep_beep2643   160 Apr  2 19:04 .docker
drwxr-xr-x  10 beep_beep2643  beep_beep2643   320 Apr  2 19:04 .orbstack
drwxr-xr-x   3 beep_beep2643  beep_beep2643    96 Apr  2 19:04 .ssh
drwxr-xr-x   3 beep_beep2643  beep_beep2643    96 Apr  2 19:04 .vscode
-rw-------   1 beep_beep2643  beep_beep2643   144 Apr  2 19:46 .zsh_history
drwx------   9 beep_beep2643  beep_beep2643   288 Apr  2 19:46 .zsh_sessions
drwx------+  3 beep_beep2643  beep_beep2643    96 Apr  2 19:03 Desktop
drwx------+  3 beep_beep2643  beep_beep2643    96 Apr  2 19:03 Documents
drwx------+  4 beep_beep2643  beep_beep2643   128 Apr  2 19:10 Downloads
drwx------@ 78 beep_beep2643  beep_beep2643  2496 Apr  2 19:30 Library
drwx------   3 beep_beep2643  beep_beep2643    96 Apr  2 19:03 Movies
drwx------+  3 beep_beep2643  beep_beep2643    96 Apr  2 19:03 Music
drwx------   4 beep_beep2643  beep_beep2643   160 Apr  2 19:04 OrbStack
drwx------+  4 beep_beep2643  beep_beep2643   128 Apr  2 19:03 Pictures
drwxr-xr-x+  4 beep_beep2643  beep_beep2643   128 Apr  2 19:03 Public
drwxr-xr-x   4 beep_beep2643  beep_beep2643   128 Apr  2 19:19 test-dir

**명령어 : cd test-dir**
       **touch test.txt**
       **touch README.md**
       **ls -la**
* total 0
drwxr-xr-x   4 beep_beep2643  beep_beep2643  128 Apr  2 19:19 .
drwxr-x---+ 20 beep_beep2643  beep_beep2643  640 Apr  2 19:46 ..
-rw-r--r--   1 beep_beep2643  beep_beep2643    0 Apr  2 19:19 README.md
-rw-r--r--   1 beep_beep2643  beep_beep2643    0 Apr  2 19:17 test.txt


**명령어 : rm README.md**
       **ls -la**

* total 0
drwxr-xr-x   3 beep_beep2643  beep_beep2643   96 Apr  2 19:53 .
drwxr-x---+ 20 beep_beep2643  beep_beep2643  640 Apr  2 19:46 ..
-rw-r--r--   1 beep_beep2643  beep_beep2643    0 Apr  2 19:17 test.txt


**명령어 : mv test.txt rename.txt**
       **ls -la**

* total 0
drwxr-xr-x   3 beep_beep2643  beep_beep2643   96 Apr  2 19:55 .
drwxr-x---+ 20 beep_beep2643  beep_beep2643  640 Apr  2 19:46 ..
-rw-r--r--   1 beep_beep2643  beep_beep2643    0 Apr  2 19:17 rename.txt


**명령어 : pwd**

* /Users/beep_beep2643/test-dir



**명령어: cd ..**
       **ls -la**

* total 16
drwxr-x---+ 20 beep_beep2643  beep_beep2643   640 Apr  2 19:46 .
drwxr-xr-x   7 root           admin           224 Apr  2 19:03 ..
-r--------   1 beep_beep2643  beep_beep2643     7 Apr  2 19:03 .CFUserTextEncoding
drwx------+  2 beep_beep2643  beep_beep2643    64 Apr  2 19:04 .Trash
drwxr-xr-x   5 beep_beep2643  beep_beep2643   160 Apr  2 19:04 .docker
drwxr-xr-x  10 beep_beep2643  beep_beep2643   320 Apr  2 19:04 .orbstack
drwxr-xr-x   3 beep_beep2643  beep_beep2643    96 Apr  2 19:04 .ssh
drwxr-xr-x   3 beep_beep2643  beep_beep2643    96 Apr  2 19:04 .vscode
-rw-------   1 beep_beep2643  beep_beep2643   144 Apr  2 19:46 .zsh_history
drwx------   9 beep_beep2643  beep_beep2643   288 Apr  2 19:46 .zsh_sessions
drwx------+  3 beep_beep2643  beep_beep2643    96 Apr  2 19:03 Desktop
drwx------+  3 beep_beep2643  beep_beep2643    96 Apr  2 19:03 Documents
drwx------+  4 beep_beep2643  beep_beep2643   128 Apr  2 19:10 Downloads
drwx------@ 78 beep_beep2643  beep_beep2643  2496 Apr  2 19:30 Library
drwx------   3 beep_beep2643  beep_beep2643    96 Apr  2 19:03 Movies
drwx------+  3 beep_beep2643  beep_beep2643    96 Apr  2 19:03 Music
drwx------   4 beep_beep2643  beep_beep2643   160 Apr  2 19:04 OrbStack
drwx------+  4 beep_beep2643  beep_beep2643   128 Apr  2 19:03 Pictures
drwxr-xr-x+  4 beep_beep2643  beep_beep2643   128 Apr  2 19:03 Public
drwxr-xr-x   3 beep_beep2643  beep_beep2643    96 Apr  2 19:55 test-dir

**명령어: cat rename.txt**
* Test test test

### 4.2 권한 확인

**명령어: ls -l**
* total 0
drwx------+  3 beep_beep2643  beep_beep2643    96 Apr  2 19:03 Desktop
drwx------+  3 beep_beep2643  beep_beep2643    96 Apr  2 19:03 Documents
drwx------+  4 beep_beep2643  beep_beep2643   128 Apr  2 19:10 Downloads
drwx------@ 78 beep_beep2643  beep_beep2643  2496 Apr  2 19:30 Library
drwx------   3 beep_beep2643  beep_beep2643    96 Apr  2 19:03 Movies
drwx------+  3 beep_beep2643  beep_beep2643    96 Apr  2 19:03 Music
drwx------   4 beep_beep2643  beep_beep2643   160 Apr  2 19:04 OrbStack
drwx------+  4 beep_beep2643  beep_beep2643   128 Apr  2 19:03 Pictures
drwxr-xr-x+  4 beep_beep2643  beep_beep2643   128 Apr  2 19:03 Public
drwxr-xr-x   3 beep_beep2643  beep_beep2643    96 Apr  2 20:02 test-dir

**명령어: ls -l rename.txt**
* total 8
* -rw-r--r--@ 1 beep_beep2643  beep_beep2643  14 Apr  2 20:02 rename.txt


**명령어: chmod a-w rename.txt**
       **ls -l rename.txt**
* -r--r--r--@ 1 beep_beep2643  beep_beep2643  14 Apr  2 20:02 rename.txt


**명령어: chmod u+x rename.txt**
       **ls -l rename.txt**
* -r-xr--r--@ 1 beep_beep2643  beep_beep2643  14 Apr  2 20:02 rename.txt


**명령어: ls -ld rnjsgks-dir**
* drwxr-xr-x  2 beep_beep2643  beep_beep2643  64 Apr  2 20:13 rnjsgks-dir


**명령어: chmod a-x rnjsgks-dir**
       **ls -ld rnjsgks-dir**
* drw-r--r--  2 beep_beep2643  beep_beep2643  64 Apr  2 20:13 rnjsgks-dir


### 4.3 Docker 설치 및 기본 점검

**명령어:docker --version**
* Docker version 28.5.2, build ecc6942

**명령어:docker ps**
* CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES

**명령어:docker info**
* Client:
 Version:    28.5.2
 Context:    orbstack
 Debug Mode: false
 Plugins:
  buildx: Docker Buildx (Docker Inc.)
    Version:  v0.29.1
    Path:     /Users/beep_beep2643/.docker/cli-plugins/docker-buildx
  compose: Docker Compose (Docker Inc.)
    Version:  v2.40.3
    Path:     /Users/beep_beep2643/.docker/cli-plugins/docker-compose

* Server:
 Containers: 1
  Running: 0
  Paused: 0
  Stopped: 1
 Images: 1
 Server Version: 28.5.2
 Storage Driver: overlay2
  Backing Filesystem: btrfs
  Supports d_type: true
  Using metacopy: false
  Native Overlay Diff: true
  userxattr: false
 Logging Driver: json-file
 Cgroup Driver: cgroupfs
 Cgroup Version: 2
 Plugins:
  Volume: local
  Network: bridge host ipvlan macvlan null overlay
  Log: awslogs fluentd gcplogs gelf journald json-file local splunk syslog
 CDI spec directories:
  /etc/cdi
  /var/run/cdi
 Swarm: inactive
 Runtimes: io.containerd.runc.v2 runc
 Default Runtime: runc
 Init Binary: docker-init
 containerd version: 1c4457e00facac03ce1d75f7b6777a7a851e5c41
 runc version: d842d7719497cc3b774fd71620278ac9e17710e0
 init version: de40ad0
 Security Options:
  seccomp
   Profile: builtin
  cgroupns
 Kernel Version: 6.17.8-orbstack-00308-g8f9c941121b1
 Operating System: OrbStack
 OSType: linux
 Architecture: x86_64
 CPUs: 6
 Total Memory: 15.67GiB
 Name: orbstack
 ID: e701612f-354f-403f-b847-735aa3e5dcd6
 Docker Root Dir: /var/lib/docker
 Debug Mode: false
 Experimental: false
 Insecure Registries:
  ::1/128
  127.0.0.0/8
 Live Restore Enabled: false
 Product License: Community Engine
 Default Address Pools:
   Base: 192.168.97.0/24, Size: 24
   Base: 192.168.107.0/24, Size: 24
   Base: 192.168.117.0/24, Size: 24
   Base: 192.168.147.0/24, Size: 24
   Base: 192.168.148.0/24, Size: 24
   Base: 192.168.155.0/24, Size: 24
   Base: 192.168.156.0/24, Size: 24
   Base: 192.168.158.0/24, Size: 24
   Base: 192.168.163.0/24, Size: 24
   Base: 192.168.164.0/24, Size: 24
   Base: 192.168.165.0/24, Size: 24
   Base: 192.168.166.0/24, Size: 24
   Base: 192.168.167.0/24, Size: 24
   Base: 192.168.171.0/24, Size: 24
   Base: 192.168.172.0/24, Size: 24
   Base: 192.168.181.0/24, Size: 24
   Base: 192.168.183.0/24, Size: 24
   Base: 192.168.186.0/24, Size: 24
   Base: 192.168.207.0/24, Size: 24
   Base: 192.168.214.0/24, Size: 24
   Base: 192.168.215.0/24, Size: 24
   Base: 192.168.216.0/24, Size: 24
   Base: 192.168.223.0/24, Size: 24
   Base: 192.168.227.0/24, Size: 24
   Base: 192.168.228.0/24, Size: 24
   Base: 192.168.229.0/24, Size: 24
   Base: 192.168.237.0/24, Size: 24
   Base: 192.168.239.0/24, Size: 24
   Base: 192.168.242.0/24, Size: 24
   Base: 192.168.247.0/24, Size: 24
   Base: fd07:b51a:cc66:d000::/56, Size: 64

WARNING: DOCKER_INSECURE_NO_IPTABLES_RAW is set


### 4.4 Docker 기본 운영 명령 수행

**명령어:docker image**
* Usage:  docker image COMMAND

* Manage images

* Commands:
  build       Build an image from a Dockerfile
  history     Show the history of an image
  import      Import the contents from a tarball to create a filesystem image
  inspect     Display detailed information on one or more images
  load        Load an image from a tar archive or STDIN
  ls          List images
  prune       Remove unused images
  pull        Download an image from a registry
  push        Upload an image to a registry
  rm          Remove one or more images
  save        Save one or more images to a tar archive (streamed to STDOUT by default)
  tag         Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE

* Run 'docker image COMMAND --help' for more information on a command.

**명령어:docker ps**
* CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES

**명령어:docker ps -a**
* CONTAINER ID   IMAGE         COMMAND    CREATED             STATUS                         PORTS     NAMES
*39ad7fe7b647   hello-world   "/hello"   About an hour ago   Exited (0) About an hour ago             determined_brattain



### 4.5 Docker 컨테이너 실행 실습

**명령어: docker run hello-world**
> Hello from Docker!
> This message shows that your installation appears to be working correctly.

> To generate this message, Docker took the following steps:
>  1. The Docker client contacted the Docker daemon.
>  2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

* To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

* Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

* For more examples and ideas, visit:
 https://docs.docker.com/get-started/


**명령어: docker run -it ubuntu**
* Unable to find image 'ubuntu:latest' locally
* latest: Pulling from library/ubuntu
* 817807f3c64e: Pull complete 
* Digest: sha256:186072bba1b2f436cbb91ef2567abca677337cfc786c86e107d25b7072feef0c
* Status: Downloaded newer image for ubuntu:latest
* root@4240b2a65f1f:/# 

**명령어: ls**
* bin   dev  home  lib64  mnt  proc  run   srv  tmp  var
* boot  etc  lib   media  opt  root  sbin  sys  usr

**명령어:cat /etc/os-release**
* PRETTY_NAME="Ubuntu 24.04.4 LTS"
* NAME="Ubuntu"
* VERSION_ID="24.04"
* VERSION="24.04.4 LTS (Noble Numbat)"
* VERSION_CODENAME=noble
* ID=ubuntu
* ID_LIKE=debian
* HOME_URL="https://www.ubuntu.com/"
* SUPPORT_URL="https://help.ubuntu.com/"
* BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
* PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
* UBUNTU_CODENAME=noble
* LOGO=ubuntu-logo


**명령어:echo "2 + 2 = 4"**

* 2 + 2 = 4


**명령어:exit**
       **docker ps**

* exit
* CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES


**명령어:docker attach my-ubuntu**
       **exit**
       **docker ps**
* CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES


**명령어:docker start my-ubuntu**
       **docker exec -it my-ubuntu bash**
       **exit**
       **docker ps**
* CONTAINER ID   IMAGE     COMMAND       CREATED          STATUS              PORTS     NAMES
* 6406e4767e05   ubuntu    "/bin/bash"   12 minutes ago   Up About a minute             my-ubuntu

* docker exec = 컨테이너 옆에서 새 창을 열어서 명령어 실행
* docker attach = 컨테이너 메인 화면에 직접 들어가기

---

### 4.6 Dockerfile 기반 커스텀 이미지 제작

**Dockerfile 작성**

> touch Dockerfile
> nano Dockerfile
> FROM nginx:latest
> COPY ./my-website /usr/share/nginx/html

* 별도의 웹 서버 설치 없이 정적 파일을 즉시 서비스 할 수 있어서 nginx 이미지를 베이스로 선택함. 이를 통해 Dockerfile에서 복잡한 환경 설정을 줄이고 빠르게 실행 가능한 컨테이너를 구성할 수 있음. 또한 nginx는 경량화되어 있고 정적 파일 서빙에 최적화 되어 있어 개발 및 테스트 환경에서 효율적으로 사용할 수 있음

* COPY 명령어 사용 이유 : COPY 명령어를 사용하여 호스트의 my-website 디렉토리를 컨테이너 내부 /usr/share/nginx/html 경로로 복사함. 해당 경로는 nginx의 기본 웹 루트 디렉토리로, 별도의 설정 없이도 웹 페이지가 바로 서비스되도록 하기 위함임. 또한 이미지 빌드 시 정적 파일을 포함시킴으로써 어디서 실행하더라도 동일한 결과를 보장할 수 있도록 구성함







* 바인드 마운트 사용 이유 : -v 옵션 사용하여 호스트의 ~/my-website 디렉토리를 컨테이너 내부 /usr/share/nginx/html 경로에 연결함. 이를 통해 컨테이너를 재빌드 하지 않고도 호스트에서 파일을 수정하면 즉시 웹 서버에 반영되도록 구성함


**명령어:docker pull nginx:latest**
> latest: Pulling from library/nginx
> ec781dee3f47: Pull complete 
> bb3d0aa29654: Pull complete 
> 510ddf6557d6: Pull complete 
> cde7a05ae428: Pull complete 
> 587e3d84dbb5: Pull complete 
> 3189680c601f: Pull complete 
> 5e815e07e569: Pull complete 
> Digest: sha256:7150b3a39203cb5bee612ff4a9d18774f8c7caf6399d6e8985e97e28eb751c18
> Status: Downloaded newer image for nginx:latest
> docker.io/library/nginx:latest


**명령어:docker images | grep nginx**
* nginx         latest    0cf1d6af5ca7   8 days ago    161MB


**명령어:docker run -d --name my-nginx -p 8080:80 nginx:latest**
       **docker ps**
* CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS          PORTS                                     NAMES
* 58c46ee6d2a8   nginx:latest   "/docker-entrypoint.…"   2 minutes ago    Up 2 minutes    0.0.0.0:8080->80/tcp, [::]:8080->80/tcp   my-nginx
* 6406e4767e05   ubuntu         "/bin/bash"              24 minutes ago   Up 13 minutes                                             my-ubuntu

**명령어:mkdir -p ~/my-website**

      cd ~/my-website
      cat > index.html << 'EOF'
      <!DOCTYPE html>
      <html>
      <head>
        <title> 테스트용 웹사이트</title>
      </head>
      <body>
       <h1>안녕하세요!</h1>
        <p>이것은 NGINX에서 띄운 페이지입니다.</p>
     </body>
     </html>
EOF
       cat ~/my-website/index.html**

<!DOCTYPE html>
<html>
<head>
    <title> 테스트용 웹사이트</title>
</head>
<body>
    <h1>안녕하세요!</h1>
    <p>이것은 NGINX에서 띄운 페이지입니다.</p>
</body>
</html>

**명령어:docker run -d --name my-nginx -p 8080:80 -v ~/my-website:/usr/share/nginx/html nginx**
       **docker ps**

* CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS          PORTS                                     NAMES
* 58c46ee6d2a8   nginx:latest   "/docker-entrypoint.…"   11 minutes ago   Up 11 minutes   0.0.0.0:8080->80/tcp, [::]:8080->80/tcp   my-nginx
* 6406e4767e05   ubuntu         "/bin/bash"              34 minutes ago   Up 22 minutes                                             my-ubuntu




## 4.7 트러블슈팅

### 4.7.1 트러블슈팅1 : 기본 페이지가 표시되는 문제


* 문제 : 브라우저 접속 시 내가 만든 페이지가 아닌 nginx 기본 페이지가 출력됨

* 원인 가설 : 컨테이너 내부 경로에 파일이 제대로 반영되지 않았을 것으로 추측

* 확인 : docker exec 명령어로 컨테이너 내부를 확인한 결과 /usr/share/nginx/html/ 경로에 기존 index.html이 존재함을 확인함

> docker exec my-nginx ls -la /usr/share/nginx/html/
> total 8
> drwxr-xr-x 1 root root  36 Mar 24 22:12 .
> drwxr-xr-x 1 root root   8 Mar 24 22:12 ..
> -rw-r--r-- 1 root root 497 Mar 24 15:38 50x.html
> -rw-r--r-- 1 root root 896 Mar 24 15:38 index.html


* 해결 : 기존 컨테이너 삭제 후 -v 옵션을 사용하여 호스트 디렉토리를 다시 마운트하여 해결함


* docker stop my-nginx
* docker rm my-nginx
* docker run -d --name my-nginx -p 8080:80 -v ~/my-website:/usr/share/nginx/html nginx:latest

* 새 브라우저 창에서 http://localhost:8080 접속

### 4.7.2. 트러블슈팅2

* 문제 : 한글 깨짐

* 해결 : nano ~/my-website/index.html


<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>테스트용 웹사이트</title>
</head>
<body>
    <h1>안녕하세요!</h1>
    <p>이것은 NGINX에서 띄운 페이지입니다.</p>
</body>
</html>







