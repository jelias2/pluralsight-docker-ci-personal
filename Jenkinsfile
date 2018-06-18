pipeline {
    agent any {


      docker {
        image 'node:6.3' }
      }

      environment{
        DOCKER_HUB_TRIGGER:  curl -H "Content-Type: application/json" --data '{"build": true}' -X POST https://registry.hub.docker.com/u/jellydones/pluralsight-docker-ci-personal
      }


    stages {
        stage('Build') {
            steps {
              echo 'Building...'
              sh 'npm --version'
            }
        }
        stage('Test'){
          steps{
            echo 'Testing...'
            sh 'node --version'
          }
        }
        stage('Deploy'){
          echo 'Deploying...'
        }
    }


    post{
      always{
        echo 'This will always run'
      }
      failure{
        echo 'Build was not successful'
      }
      success{
        echo 'Build was successful'
      }
    }
}

// sh commands may need to change to bat commands
