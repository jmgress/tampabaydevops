pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'BuildStage'
      }
    }
    stage('CodeQuality') {
      steps {
        echo 'Add SonarQube'
      }
    }
    stage('Testing') {
      steps {
        echo 'TestingPhase '
      }
    }
    stage('Email Success ') {
      steps {
        emailext(subject: 'Success', body: 'Success', from: 'me@me.com', to: 'jamesgress@hotmail.com', replyTo: 'me@me.com')
      }
    }
  }
}