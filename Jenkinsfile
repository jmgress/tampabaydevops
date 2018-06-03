pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'BuildStage'
        sh '''echo "Starting"
#shuf -i 2000-65000 -n 1
thewinner=1
echo "The Winner is : " $thewinner'''
      }
    }
  }
}