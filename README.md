# video-mp3-converter
System design of a micro-service architecture for video to mp3 converter in python
## Installation
- Install Docker Desktop
  - https://www.docker.com/products/docker-desktop/
  - https://learn.microsoft.com/en-us/windows/wsl/- - -    install-manual#step-4---download-the-linux-kernel-update-package
  - cmd: docker --version (check for installation)
  - (https://forums.docker.com/t/restart-docker-service-from-command-line/27331)

- Install kubectl
  - https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/
  - choco install kubernetes-cli (powershell - admin mode)
  - kubectl (verify)

- Install minikube
  https://minikube.sigs.k8s.io/docs/start/ (install exe) 
   minikube is local Kubernetes, focusing on making it easy to learn and develop for Kubernetes.
  - minikube start (verify) - first run docker desktop then run this command

    result (
         * minikube v1.28.0 on Microsoft Windows 10 Enterprise 10.0.19043 Build 19043
         * Automatically selected the docker driver
         * Using Docker Desktop driver with root privileges
        * Starting control plane node minikube in cluster minikube
        * Pulling base image ...
        * Downloading Kubernetes v1.25.3 preload ...
        * Creating docker container (CPUs=2, Memory=4000MB) ...
        * Preparing Kubernetes v1.25.3 on Docker 20.10.20 ...
                - Generating certificates and keys ...
                - Booting up control plane ...
                - Configuring RBAC rules ...
        * Verifying Kubernetes components...
                - Using image gcr.io/k8s-minikube/storage-provisioner:v5
        * Enabled addons: storage-provisioner, default-storageclass
        * Done! kubectl is now configured to use "minikube" cluster and "default" namespace by default
    )

- Install K9s
  - https://k9scli.io/topics/install/
  - choco install k9s
  - k9s (verify) - it will open a pod terminal

- Install Python
  py --version (verify)

- MySql
  https://dev.mysql.com/downloads/installer/ -(mysql-installer-community) -(not-web-one)
  - install for developer default
  - root password: root
  - service name: MySQL80
  - run by default on startup
  -- TO verify, we need to add mysql.exe from mysql server to our path
     i.e. C:\Program Files\MySQL\MySQL Server 8.0\bin
      - in system variables - path - new
     - now, open new terminal & can verify with -> mysql --version
  - mysql -u root -p (to access)
    - It will ask for password & then give access to mysql
    - If password is set & we try to access without '-p', it will give access denied error
