pipeline{

	agent any

	environment {
		DOCKERHUB_CREDENTIALS=credentials('dockerhub_id')
	}

	stages {
		
		stage('build') {
			steps {
				sh'docker-compose build rafdev0904/nodejsphp:latest'
				
			}
		}

		stage('Login') {

			steps {
				sh 'docker login -u rafdev0904 -p Tkjmhd123'
			}
		}
	
		stage('Push') {

			steps {
				sh 'docker push rafdev0904/nodejsphp'
			}
		}
	}

	post {
		always {
			sh 'docker logout'
		}
	}

}
