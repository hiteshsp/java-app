pipeline {
  agent any
  stages {
    stage('git clone') {
      checkout scm
    }
    stage('Maven build') {
      steps {
        bat(script: 'cd SpringMVCSecurityXML/ && mvn clean install -Dbuild.number', returnStatus: true, returnStdout: true)
      }
    }
  }
}
