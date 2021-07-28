pipeline {
  agent {
    docker {
      image 'golang:1.14'
    }

  }
  stages {
    stage('build') {
      steps {
        sh '''sh \'sudo docker go build\'
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