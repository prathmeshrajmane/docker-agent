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

'''
      }
    }

    stage('test') {
      agent {
        dockerfile {
          filename 'Dockerfile'
        }

      }
      steps {
        sh '''sudo docker run multistage-app
'''
      }
    }

  }
}