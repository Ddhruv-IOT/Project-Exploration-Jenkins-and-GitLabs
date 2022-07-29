pipeline {

	agent any

	stages {	

		stage ('SCM') {
			steps {
				echo "git pull my code"
				git 'https://github.com/Ddhruv-IOT/simple-java-maven-app.git'
			}	
		}

		stage ('Build') {
			steps {
				echo "Pack"
				sh 'mvn clean package'
			}	
		}		

		stage ('Deploy') {
			steps { 
				echo "final step"
				sh 'java -jar target/*.jar'
			}
		}
	}
}
