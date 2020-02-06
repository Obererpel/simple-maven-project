pipeline {
	agent any
	tools {
		maven 'Maven'
	}
	stages {
		stage('Repository') {
			steps {
				echo 'Clone and checkout repository'
				git url: 'https://github.com/Obererpel/simple-maven-project.git', branch: '$BRANCH_NAME'
			}
		}
		
		stage('Build') {
			steps {
				sh 'mvn clean compile'
			}
		}
		
		stage('Test') {
			steps {
				echo 'Nothing to do'
			}
		}
		
		stage('Deploy') {
			steps {
				echo 'Nothing to do'
			}
		}
		
		stage('Clean up') {
			steps {
				echo 'Nothing to do'
			}
		}
	}
}
