pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'BuildStage'
        sh '''echo "Starting"
thewinner=$(shuf -i 190-199 -n 1)
echo "The Winner is : " $thewinner'''
      }
    }
  }
}