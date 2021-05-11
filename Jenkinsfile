pipeline {
    agent any
    stages {
        stage('Start Grid') {
            steps {
                //sh for LINUX and Bat for Windows
                bat "docker-compose up -d hub chrome firefox"
            }
        }
		stage('Run Tests') {
            steps {
                //sh
                bat "docker-compose up search-module book-flight-module"
            }
        }
        stage('Stop Grid ') {
            steps {
                //sh
                bat "docker-compose down"
            }
        }
    
    }
}