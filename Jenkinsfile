pipeline {
  agent any
  stages {
    stage('build ') {
      agent {
        dockerfile {
          filename 'Dockerfile'
        }

      }
      steps {
        sh '''sudo docker build -t multistage-app .
sudo docker run multistage-app

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