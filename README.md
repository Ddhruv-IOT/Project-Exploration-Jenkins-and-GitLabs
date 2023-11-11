# Project Exploration

This repository contains the exploration of Jenkins and GitLab for automating build and deployment processes, as well as other experiments and comparisons. In this README, we will provide an overview of the key activities and findings in this repository.

## Jenkins Exploration

### Jenkins Jobs Using Web UI

We used the Jenkins web UI to create and manage Jenkins jobs for various tasks, such as building and deploying applications. The web UI provides an intuitive way to configure and trigger Jenkins jobs.

### Jenkins Pipeline

We created a Jenkins pipeline using a Jenkinsfile to automate the build and deployment process of a Java Maven application. Below is an explanation of the Jenkinsfile:

```groovy
pipeline {
	agent any
	stages {
		stage('SCM') {
			steps {
				echo "Git pull my code"
				git 'https://github.com/Ddhruv-IOT/simple-java-maven-app.git'
			}
		}
		stage('Build') {
			steps {
				echo "Pack"
				sh 'mvn clean package'
			}
		}
		stage('Deploy') {
			steps {
				echo "Final step"
				sh 'java -jar target/*.jar'
			}
		}
	}
}
```

In this pipeline, we have three stages: SCM, Build, and Deploy. It pulls code from a Git repository, builds the Java Maven application, and deploys it.

## GitLab Exploration

We also explored GitLab and experimented with PHP and Bash code to obtain the IP address of the system. Additionally, we set up a local runner in GitLab to execute CI/CD pipelines.

## GitLab vs. Jenkins

### GitLab

- GitLab is primarily a web-based Git repository manager.
- It offers integrated CI/CD capabilities using GitLab CI/CD.
- GitLab provides a single platform for version control, issue tracking, CI/CD, and more.

### Jenkins

- Jenkins is an automation server that can be used for continuous integration and continuous delivery.
- It is highly customizable and can be extended with various plugins.
- Jenkins can be configured and managed using its web UI or by defining pipelines as code in Jenkinsfiles.

## Thank You

Thank you for exploring this repository. If you have any questions or need further assistance, please feel free to reach out.
