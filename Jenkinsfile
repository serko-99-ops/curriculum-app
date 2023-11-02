pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        git(url: 'https://github.com/serko-99-ops/curriculum-app', branch: 'dev', credentialsId: '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')
      }
    }

  }
}