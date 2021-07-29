
pipeline {
    agent none
    stages {
        stage('build and test') {
            agent { docker { image 'golang:1.14' } }
            environment {
                GOCACHE = '/tmp/gocache'
            }
            steps {
                sh 'go build'
                sh 'go test ./...'
            }
        }
    }
