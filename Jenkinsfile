pipeline {
	agent any
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}

	stages {
		stage('Checkout') {
			steps {
				sh 'mvn --version'
				sh 'docker --version'
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

		stage('Build') {
			steps {
				sh 'mvn clean compile'
			}
		}

		stage('Test') {
			steps {
				sh 'mvn test'
			}
		}

		stage('Integration Test') {
			steps {
				sh "mvn failsafe:integration-test failsafe:verify"
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
