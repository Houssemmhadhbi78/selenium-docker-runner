pipeline {
    agent any
    stages {
        stage('Run Test') {
            steps {
                //sh
                bat "docker-compose up"
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