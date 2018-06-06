pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Stage'
      }
    }
    stage('Test Firefox') {
      parallel {
        stage('Test Firefox') {
          steps {
            echo 'Test FireFox'
          }
        }
        stage('Test IE') {
          steps {
            echo 'Test IE'
          }
        }
      }
    }
    stage('Run It') {
      steps {
        sh '''echo "Starting"
thewinner=$(shuf -i 1-10 -n 1)
echo "The Winner is : " $thewinner

thewinner=$(shuf -i 1-10 -n 1)
echo "The Winner is : " $thewinner

thewinner=$(shuf -i 1-10 -n 1)
echo "The Winner is : " $thewinner

thewinner=$(shuf -i 1-10 -n 1)
echo "The Winner is : " $thewinner

thewinner=$(shuf -i 1-10 -n 1)
echo "The Winner is : " $thewinner

thewinner=$(shuf -i 1-10 -n 1)
echo "The Winner is : " $thewinner

thewinner=$(shuf -i 1-10 -n 1)
echo "The Winner is : " $thewinner

thewinner=$(shuf -i 1-10 -n 1)
echo "The Winner is : " $thewinner

thewinner=$(shuf -i 1-10 -n 1)
echo "The Winner is : " $thewinner

thewinner=$(shuf -i 1-10 -n 1)
echo "The Winner is : " $thewinner
'''
      }
    }
  }
}