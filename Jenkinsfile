pipeline {
    agent any

    stages {

        stage('Clone Repo') {
            steps {
                git branch: 'main' 'https://github.com/sanskruti142003-beep/practise.git/
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myapp:v1 .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d --name mycontainer myapp:v1'
            }
        }
    }
