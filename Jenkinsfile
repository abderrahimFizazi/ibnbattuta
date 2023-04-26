pipeline {
  agent any
  environment{
    NEW_VERSION = "1.20.11"
    DB_CREDENTIALS = credentials("db-server")
  }
  stages {
    stage("deploy") {
      steps {
        echo 'Deploying the app..'
        sh 'docker-compose up'
      }
    }
  }
}
