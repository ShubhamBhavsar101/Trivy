# Trivy

Trivy helps to find known vulnerabilities, misconfigurations in IAC, Sensitive information and Secrets, Issues with docker images, etc

Trivy can be used with container image, filesystem/folders, Git repository, Virtual Machine Image, Kubernetes and AWS

## Installation
### Install Docker
```bash
sudo apt update
sudo apt install docker.io -y
```

### Install Trivy
```bash
sudo apt-get install wget apt-transport-https gnupg lsb-release
wget -qO - https://aquasecurity.github.io/trivy-repo/deb/public.key | sudo apt-key add -
echo deb https://aquasecurity.github.io/trivy-repo/deb $(lsb_release -sc) main | sudo tee -a /etc/apt/sources.list.d/trivy.list
sudo apt-get update
sudo apt-get install trivy -y
```

### Commands
```
trivy image nginx 
```
```
trivy image --severity HIGH,CRITICAL nginx
```
```
trivy fs --security-checks vuln,config folder
```
```
trivy image -f json -o results.json jenkins/jenkins
```


