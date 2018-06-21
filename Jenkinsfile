node  {
  docker.image('node:7-alpine').inside{
  // ('linux') ^^
  //    withEnv([
  //    DOCKER_HUB_TRIGGER='curl -H "Content-Type: application/json" --data \'{"build": true}\' -X POST https://registry.hub.docker.com/u/jellydones/pluralsight-docker-ci-personal'
  //      ])

      stage('Build') {

            echo 'Building...'
  	  sh 'docker version'
  	  sh 'docker build -t nvm'
  	  sh 'docker images'
  	  sh 'docker run -it nvm bash'
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
}
