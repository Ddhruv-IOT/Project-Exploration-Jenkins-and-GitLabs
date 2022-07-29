pipeline {

	agent any

	stages {	

		stage ('SCM') {
			steps {
				echo "git pull my code"
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
