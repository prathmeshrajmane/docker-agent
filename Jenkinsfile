pipeline {
  agent none
  stages {
    stage('build') {
      agent {
        docker {
          image 'golang:1.14'
        }

      }
      environment {
        GOCACHE = '/tmp/gocache'
      }
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
}