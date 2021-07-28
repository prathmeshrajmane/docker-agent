pipeline {
  agent {
    docker {
      image 'image \'golang:1.14'
    }

  }
  stages {
    stage('build') {
      steps {
        sh '''sh \'go build\'
'''
      }
    }

    stage('test') {
      steps {
        sh ''' sh \'go test ./...\'
'''
      }
    }

  }
  environment {
    GOCACHE = '/tmp/gocache'
  }
}