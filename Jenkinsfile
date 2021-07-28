pipeline {
  agent {
    docker {
      image 'centos'
    }

  }
  stages {
    stage('build ') {
      agent any
      steps {
        sh '''sudo docker build -t multistage-app .
'''
      }
    }

    stage('Run container') {
      steps {
        sh '''sh docker run multistage-app
'''
      }
    }

    stage('test') {
      steps {
        sh 'echo "success"'
      }
    }

  }
}