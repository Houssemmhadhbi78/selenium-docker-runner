pipeline {
    agent any
    stages {
		stage('Pull Latest Image hmhadhbi84') {
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
	post('Stop Grid with Post') {
		always{
			archiveArtifacts artifacts: 'output/**'
			bat "docker-compose down"
		}
	}
}