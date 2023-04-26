pipeline {
  agent any
  environment{
    NEW_VERSION = "1.20.11"
  }
  stages {
    stage("deploy") {
      steps {
        echo 'Deploying the app..'
        sh 'docker-compose up -d && timeout 60 docker-compose logs -f && docker-compose down'
      }
    }
  }
}
