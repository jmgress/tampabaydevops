pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'BuildStage'
        sh '''echo "Starting"
thewinner=$(shuf -i 500-2000 -n 1)
echo "The Winner is : " $thewinner'''
      }
    }
  }
}