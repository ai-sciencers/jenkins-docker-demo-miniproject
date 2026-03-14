pipeline {
 agent { label 'built-in' }
 stages {
   stage('clone repository') {
    steps {
     git 'url'
    }
}
   stage('Docker build image') {
    steps {
     sh 'docker build -t jenkins-demo .'
    }
}
  stage('run container') {
   steps {
   sh 'docker run -d -p 8080:80 --name jenkins-container jenkins-demo'
      }      
}

    }
}
