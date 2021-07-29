pipeline {
  agent {
    docker {
      image 'golang:1.14'
    }

  }
  stages {
    stage('build') {
      steps {
        sh 'go build -a -installsuffix cgo -o main .'
      }
    }

    stage('Run') {
      steps {
        sh './main'
      }
    }

  }
  environment {
    GOCACHE = '/tmp/gocache'
  }
}