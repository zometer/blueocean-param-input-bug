pipeline {
  agent any
  stages {
    stage('Do stuff...') {
      steps {
        echo "params: $params"
        sh 'env'
      }
    }
    stage('Complete') {
      steps {
        sh 'env'
      }
    }
  }
  parameters {
    choice(choices: '''CI
DEV
PROD''', description: 'Is this a DEV or a PROD build?', name: 'BUILD_TYPE')
    text(description: 'Release Notes (Type "t" to switch focus to search bar.)', name: 'RELEASE_NOTES', defaultValue: 'CI Build')
  }
}