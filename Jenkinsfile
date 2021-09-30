pipeline {
  agent any
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    stage('Scan') {
      steps {
        withSonarQubeEnv(installationName: 'Sonar-DLab'){
          sg 'mvn clean sonar:sonar -Dsonar.login=myAuthenticationToken'
        }
      }
    }
    }
    }
