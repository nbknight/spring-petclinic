pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Pull latest code base'
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''./mvn sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.projectName=\'Petclinic\' \\
  -Dsonar.host.url=http://172.31.91.28:9000 \\
  -Dsonar.token=sqp_ffc6f95d6c9c72ce849ea29ea28d6a6ca791f68b'''
      }
    }

  }
}