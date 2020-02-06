pipeline {
	agent any
	def mvnHome = tool 'Maven'
	stages {
		stage('Repository') {
			steps {
				echo 'Clone and checkout repository'
				git url: 'https://github.com/Obererpel/simple-maven-project.git', branch: '$BRANCH_NAME'
			}
		}
		
		stage('Build') {
			steps {
				withEnv(["MVN_HOME=$mvnHome"]) {
					if (isUnix()) {
						sh '"$MVN_HOME/bin/mvn" clean compile'
					} else {
						bat(/"%MVN_HOME%\bin\mvn" clean compile/)
					}
				  }
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
