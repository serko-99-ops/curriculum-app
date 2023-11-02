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
            sh 'cd curriculum-front && npm i  && npm run test:unit'
          }
        }

      }
    }

  }
}