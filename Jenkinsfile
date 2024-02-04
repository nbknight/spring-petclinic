pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Pull latest code base'
        sh './mvnw clean compile'
      }
    }

  }
}