pipeline {
  agent any
  environment{
    NEW_VERSION = "1.20.11"
  }
  stages {
    stage("deploy") {
      steps {
        echo 'Deploying the app..'
        sh '''
          docker stop first
          docker rm first
          docker-compose up -d --no-color --wait
          docker compose ps
        '''
      }
    }
  }
}
