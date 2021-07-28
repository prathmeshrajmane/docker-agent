pipeline {
  agent {
    docker {
      image 'centos'
    }

  }
  stages {
    stage('build ') {
      agent {
        docker {
          image 'nginx:alpine'
        }

      }
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