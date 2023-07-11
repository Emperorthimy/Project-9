# **Documentation for Project 9**

### Installing JDK

`sudo apt update`
`sudo apt install default-jdk-headless`

![JDk-Installation](./Images/install-jdk.png)

![JDk-Installation](./Images/jdk-lib.png)

### Jenkins Installation

`sudo apt update`
```
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```

![Jenkins-Installation](./Images/install-jenkins&dependecies.png)

![Jenkins-Installation](./Images/jenkins&dependecies.png)

### Jenkins Up and running

`sudo systemctl status jenkins`

![Making-sure-Jenkins-is-up-and-running](./Images/jenkins-status.png)

## Jenkins Initial Setup

### Accessing jenkings from Browser

`http://<Jenkins-Server-Public-IP-Address-or-Public-DNS-Name>:8080`

![Accessing-Jenkins-from-Browser](./Images/accessing-jenkins.png)

### Jenkins Setup Complete

![Jenkins-setup-complete](./Images/jenkins-ready.png)

## Connecting Jenkins to Github to retrieve source Codes using Webhooks

![successfully-enabled-webhooks](./Images/github-webhook.png)

### First Successful Jenkins Build

![First-Jenkins-Build](./Images/job1-build.png)

### Post Build Action Configuration

![New-Build-Triggered-after-postBuild-Action-configuration](./Images/console-output-build-2.png)

### Location of artifacts on Jenkins Server

`ls /var/lib/jenkins/jobs/Project9/builds/2/archive/`

![Artifacts-Location-on-Jenkins-server](./Images/artifacts-location.png)

## Configuring jenkins to copy files to NFS Server Via SSH

### Publish over SSH plugin Installation

![publish-over-ssh-plugin-installation](./Images/publish-over-ssh-plugins.png)

### Configuring projects to copy artifacts over to NFS

### Jenkins configured to send all files produced by build to mnt/apps

![copying-artifacts-over-to-NFS](./Images/post-build-ssh.png)

![Artifacts-Location-on-Jenkins-server](./Images/postbuild-action.png)

![Artifacts-Location-on-Jenkins-server](./Images/send-artifacts-to-nfs.png)

### Console output after changes has been made to read-me

![Console-output-after-changes-have-been-made-to-readme](./Images/cat-readme.png)

### Making sure files are updated on NFS Server Successfully

![files-updated-on-NFS-server-successfully](./Images/artifacts-location.png)

![Artifacts-Location-on-Jenkins-server](./Images/console-output-build-5.png)