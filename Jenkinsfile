pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'BuildStage'
        sh '$(( ( RANDOM % 10 )  + 1 ))'
      }
    }
  }
}