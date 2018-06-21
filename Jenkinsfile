node  {
// ('linux') ^^
//    withEnv([
//    DOCKER_HUB_TRIGGER='curl -H "Content-Type: application/json" --data \'{"build": true}\' -X POST https://registry.hub.docker.com/u/jellydones/pluralsight-docker-ci-personal'
//      ])

    stage('Build') {

          echo 'Building...'
          sh 'npm --version'

    }
    stage('Test'){

        echo 'Testing...'
        sh 'node --version'

    }
    stage('Deploy'){
      echo 'Deploying...'
      sh 'curl -H "Content-Type: application/json" --data \'{"build": true}\' -X POST https://registry.hub.docker.com/u/jellydones/pluralsight-docker-ci-personal'
    }


}
