pipeline {
  agent any
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    stage('Scan') {
      steps {
        withSonarQubeEnv(installationName: 'mysonar') { 
          sh './mvnw sonar:sonar'
        }
      }
    }
  }
}
