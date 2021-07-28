pipeline {
  agent {
    docker {
      image 'golang:1.14'
    }

  }
  stages {
    stage('build ') {
      steps {
        sh '''sh \'docker build -t simple-nginx .\'
'''
      }
    }

    stage('Run container') {
      steps {
        sh 'sh \'docker run -d -it -p 8080:80 simple-nginx\''
      }
    }

  }
  environment {
    GOCACHE = '/tmp/gocache'
  }
}