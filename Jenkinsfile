pipeline {

	agent any

	stages {	

		stage ('SCM') {
			steps {
				echo "git pull my code"
				git 'https://github.com/Ddhruv-IOT/Jenkins-repo-1.git'
			}	
		}

		stage ('Deploy') {
			steps {
				echo "Deploy"
			}	
		}		

		stage ('Test') {
			steps { 
				echo "final test"
			}
		}
	}
}
