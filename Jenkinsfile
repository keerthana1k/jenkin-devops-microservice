//SCRIPTED PIPELINE

// node {
// 		echo "Build"
// 		echo "Test"
// 		echo "Integration Test"	
// }


//DESLARATIVE
pipeline {
	//agent any
	//agent { docker { image 'maven:3.9.11'}}
	//agent { docker { image 'node:24.9.0'}}
	stages {
		stage('Build') {
			steps {
				//sh "mvn --version"
				//sh 'node --version'
				echo "Build"
				echo "$PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"
			}
		}
		stage('Test') {
			steps {
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
			echo 'I, awesome. I run always'
		}
		success {
			echo 'I run when you are successful'
		}
		failure {
			echo 'I run when you are Fail'
		}
		//unstable
		//changed
	}
}