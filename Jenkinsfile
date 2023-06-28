pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo "Pre-Build"
				echo "Build"
			}
		}
		stage('Test') {
			steps {
				echo "Pre-Test"
				echo "Test"
			}
		}

		stage('Integration Test') {
			steps {
				echo "Integration Test"
			}	
		}
	} 
	
	post {
		always {
			echo 'This is awesome'
		}

		success {
			echo 'This is awesome. Success'
		}

		failure {
			echo 'This is awesome. Failure'
		}
	}

	
}
