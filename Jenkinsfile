pipeline {
  agent {
    docker {
      image 'golang:1.14'
    }

  }
  stages {
    stage('build') {
      steps {
        sh '''go get -u github.com/ponzu-cms/ponzu/...
go build'''
      }
    }

    stage('test') {
      steps {
        sh 'go test ./...'
      }
    }

  }
  environment {
    GOCACHE = '/tmp/gocache'
  }
}