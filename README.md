<img src="https://github.com/Harsh971/Python-System-Monitor-Webapp-CICD/blob/main/architecture.gif"></img>

# Python Flask - Demo Web Application

This is a simple Python Flask web application. The app provides system information and a realtime monitoring screen with dials showing CPU, memory, IO and process information.

## Screenshot

![screen](https://user-images.githubusercontent.com/14982936/30533171-db17fccc-9c4f-11e7-8862-eb8c148fedea.png)

### Makefile

In DevOps, a `Makefile` is a script used by the make tool to automate tasks such as building, testing, and deploying applications. It defines a set of rules and dependencies to ensure that tasks are executed in the correct order, facilitating consistent and repeatable processes across different environments.

```text
help                 💬 This help message
lint                 🔎 Lint & format, will not fix but sets exit code on error
lint-fix             📜 Lint & format, will try to fix errors and modify code
image                🔨 Build container image from Dockerfile
push                 📤 Push container image to registry
run                  🏃 Run the server locally using Python & Flask
deploy               🚀 Deploy to Azure Web App
undeploy             💀 Remove from Azure
test                 🎯 Unit tests for Flask app
test-report          🎯 Unit tests for Flask app (with report output)
test-api             🚦 Run integration API tests, server must be running
clean                🧹 Clean up project
```

Essential Jenkins Plugins
----------

- `jdk` : Eclipse Temurin installer
- `sonar` : SonarQube Scanner
- `owasp` : OWASP Dependency-Check
- `docker` : Docker, Docker Pipeline

## Configuration of Plugins

### Configure Plugins : 
- Manage Jenkins > Global Tool Configuration

### JDK Installation
- Name : jdk17
- Install Automatically > Install from adoptium.net > Version 17

### SonarQube Scanner installations
- Name : sonar-scanner
- Install Automatically > Version (Default)

### Dependency-Check installations
- Name : DP
- Install Automatically > Install from github.com > dependency-check 6.5.1

### Docker installations
- Name : docker
- Install Automatically > Version (latest)

## Jenkinsfile Prerequisite : 
- for the stage named : *Trivy* we need to have trivy established into our Environmental System
```
sudo apt-get install wget apt-transport-https gnupg lsb-release

wget -qO - https://aquasecurity.github.io/trivy-repo/deb/public.key | gpg --dearmor | sudo tee /usr/share/keyrings/trivy.gpg > /dev/null

echo "deb (signed-by=/usr/share/keyrings/trivy.gpg) https://aquasecurity.github.io/trivy-repo/deb $(lsb_release -sc) main" | sudo tee -a /etc/apt/sources.list.d/trivy.list

sudo apt-get update

sudo apt-get install trivy -y
```

## Source Credits :
Original Source Code : [Click Here](https://github.com/jaiswaladi246/Python-Webapp)
<br>
Tutorial Reference : [Click Here](https://www.youtube.com/watch?v=atjrbzPqG8c&list=PLAdTNzDIZj_9C6qKZ3wE8t97OXqUZkzpB&index=5&pp=iAQB)

## Feedback

Your feedback is valuable! If you have suggestions for improving existing content or ideas for new additions, please open an issue or reach out to the repository maintainers. If you have any other feedbacks, you can reach out to us at harsh.thakkar0369@gmail.com


## Connect with Me
<p>

 <a href="https://twitter.com/HarshThakkar971" target="blank"><img align="center" src="https://img.freepik.com/premium-vector/vector-new-twitter-x-white-logo-black-background_744381-866.jpg" alt="HarshThakkar971" height="40" width="50" /></a>
  &nbsp;&nbsp;
  	<a href="https://linkedin.com/in/harsh-thakkar-7764bb1a4" target="blank"><img align="center" src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/LinkedIn_logo_initials.png/800px-LinkedIn_logo_initials.png" alt="harsh-thakkar-7764bb1a4" height="40" width="40" /></a>
  &nbsp;&nbsp;
 <a href="https://instagram.com/harsh_thakkar09" target="blank"><img align="center" src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e7/Instagram_logo_2016.svg/768px-Instagram_logo_2016.svg.png" alt="harsh_thakkar09" height="40" width="40" /></a>
</p>
