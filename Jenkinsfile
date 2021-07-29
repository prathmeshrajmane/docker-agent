pipeline {
  agent none
  stages {
    stage('build') {
      agent {
        docker {
          image 'golang:1.12.0'
        }

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