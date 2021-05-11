pipeline {
    agent any
    stages {
        stage('Run Test') {
            steps {
                //sh
                bat "docker-compose up -d --scale chrome=4 --scale firefox=5"
            }
        }
        stage('Bring Grid Down') {
            steps {
                //sh
                bat "docker-compose down"
            }
        }
    
    }
}