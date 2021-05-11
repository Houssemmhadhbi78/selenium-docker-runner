pipeline {
    agent any
    stages {
		stage('Pull Latest Image') {
            steps{
				bat "docker pull hmhadhbi84/selenium-docker"
			}
		}
        stage('Start Grid') {
            
			steps {
                //sh for LINUX and Bat for Windows
                bat "docker-compose up -d hub chrome firefox"
            }
        }
		stage('Run Tests') {
            steps {
                //sh
                bat "docker-compose up --no-color search-module book-flight-module"
            }
        }
	}
	post('Stop Grid') {
		always{
			bat "docker-compose down"
		}
	}
}