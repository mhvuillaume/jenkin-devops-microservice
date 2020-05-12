// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 		stage('IntegrationTest') {
// 		echo "IntegrationTest"
// 	}
// }

pipeline {
	agent { docker {image 'maven:3.6.3'} }
	stages{
		stage('Build') {
			steps {
				sh 'mvn --version'
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
			echo "post - always"
		}
		success {
			echo "post - success"
		}
		failure {
			echo "post - failure"
		}
	}
}