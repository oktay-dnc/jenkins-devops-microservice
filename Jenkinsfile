pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo "$PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BRANCH_NAME - $env.BRANCH_NAME"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "BUILD_URL - $env.BUILD_URL"
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
