pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        git(url: 'https://github.com/serko-99-ops/curriculum-app', branch: 'dev')
      }
    }

    stage('check') {
      parallel {
        stage('check') {
          steps {
            sh 'ls -la'
          }
        }

        stage('front') {
          steps {
            sh 'cd curriculum-front '
          }
        }

        stage('error') {
          steps {
            sh 'ls'
          }
        }

      }
    }

    stage('docker') {
      environment {
        DOCKERHUB_USER = 'serko231'
        DOCKERHUB_PASSWORD = 'Serega1722!'
      }
      steps {
        sh '''docker login -u $DOCKERHUB_USER -p $DOCKERHUB_PASSWORD





'''
      }
    }

    stage('ls') {
      steps {
        sh 'ls -la'
      }
    }

  }
  environment {
    DOCKERHUB_USER = 'serko231'
    DOCKERHUB_PASSWORD = 'Serega1722!'
  }
}