pipeline {
	agent {
		docker {
			image 'maven:3.6.3'
		}
	}
	stages {
		stage('Build') {
			steps {
				sh "mvn --version"
				sh "ls -al"
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
