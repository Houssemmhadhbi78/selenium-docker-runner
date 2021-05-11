pipeline {
    agent any
    stages {
        stage('Start Grid') {
            steps {
                //sh for LINUX and Bat for Windows
                bat "docker-compose up -d hub chrome firefox --scale chrome=3 --scale firefox=3"
            }
        }
		stage('Run Tests') {
            steps {
                //sh
                bat "docker-compose up search-module book-flight-module --no-color"
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