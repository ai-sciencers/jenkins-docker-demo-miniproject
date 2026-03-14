pipeline {
    agent { label 'built-in' }

    stages {

        stage('Docker build image') {
            steps {
                sh 'docker build -t jenkins-demo .'
            }
        }

        stage('remove old container') {
            steps {
                sh 'docker rm -f jenkins-container || true'
            }
        }

        stage('run container') {
            steps {
                sh 'docker run -d -p 8081:80 --name jenkins-container jenkins-demo'
            }
        }

    }
}
