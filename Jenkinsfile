ipipeline {
	agent {  label 'linux-node' }
	stages {
		stage('---cleaning----'){
			tools {
				maven 'maven_3.9.4'
			}
			steps {
				sh 'mvn --version'
				sh "mvn clean"
			}
		}
		stage('---testing---') {
			tools {
				maven 'maven_3.9.0'
			}
			steps {
				sh 'mvn --version'
				sh "mvn test"
			}
		}
		stage('---package---'){
			tools {
				maven 'maven_3.8.8'
			}
			
			steps {
				sh 'mvn --version'
				sh "mvn package"
			}
		}
	}
	post {
		success {
			echo 'job was built successfully'
		}
		failure {
			echo 'job was not build..it was failed'
		}
	}
}
