//SCRIPTED PIPELINE

// node {
// 		echo "Build"
// 		echo "Test"
// 		echo "Integration Test"	
// }


//DESLARATIVE
pipeline {
	//agent any
	agent { docker { image 'maven:3.9.11'}}
	stages {
		stage('Build') {
			steps {
				sh "mvn --version"
				echo "Build"
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