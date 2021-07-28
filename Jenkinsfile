pipeline {
  agent {
    docker {
      image 'nginx:alpine'
    }

  }
  stages {
    stage('build ') {
      steps {
        sh 'sudo docker pull nginx:latest'
      }
    }

    stage('Run container') {
      steps {
        sh '''sh \'docker build -t simple-nginx .\'
'''
      }
    }

    stage('test') {
      steps {
        sh 'sh \'docker run -d -it -p 8080:80 simple-nginx\''
      }
    }

  }
}