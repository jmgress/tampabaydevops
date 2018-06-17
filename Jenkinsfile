pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Stage'
        sh '''#!/bin/bash set +x

createDockerContainer() {
	echo $1, $2
    export ENVIRONMENT_NAME=$1
    export SERVICE_NAME="$(echo ${PROJECT_NAME} | tr \\\'/\\\' \\\'_\\\')_${ENVIRONMENT_NAME}"
    docker-compose -p ${SERVICE_NAME} up -d
    ## Add nginx configuration
    sed -i "s/###TOMCAT_SERVICE_NAME###/${SERVICE_NAME}/" $2
    docker cp $2 proxy:/etc/nginx/sites-enabled/${SERVICE_NAME}.conf
}

echo "Iam here"
ENVIRONMENT_TYPE=DEV

if [ "$ENVIRONMENT_TYPE" = "DEV" ]; then
 	createDockerContainer "CI" tomcat.conf
elif [ "$ENVIRONMENT_TYPE" = "PROD" ]; then
	##Creating 2 environment PRODA and PRODB, with a upstream ngix configuration in prod-tomcat.conf
    mv tomcat.conf tomcatA.conf &&cp tomcatA.conf tomcatB.conf

	echo "PRODA" , "tomcatA.conf"
    export ENVIRONMENT_NAME=$1
    export SERVICE_NAME="$(echo ${PROJECT_NAME} | tr \\\'/\\\' \\\'_\\\')_${ENVIRONMENT_NAME}"'''
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

thewinner=$(shuf -i 690388-690410 -n 1)
echo "The Winner is : " $thewinner

thewinner=$(shuf -i 1-10 -n 1)
echo "The Winner is : " $thewinner
'''
      }
    }
  }
}