pipeline {
    agent any
    stages {
        stage('Run Test') {
            steps {
                //sh
                bat "docker-compose up --scale chrome=3 --scale firefox=3 --no-color"
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