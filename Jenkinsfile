pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Shridhar0903/docker-java-jenkins.git'
            }
        }

       stage('Build Docker Image') {
    steps {
        script {
            bat 'set DOCKER_BUILDKIT=0 && docker build -t dockerized-java-app:latest .'
        }
    }
}


        stage('Run Docker Container') {
            steps {
                sh 'docker run --rm dockerized-java-app:latest'
            }
        }
    }
}
