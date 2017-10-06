pipeline {
  agent any
  stages {
    stage('git clone') {
      steps {
        git(url: 'https://github.com/hiteshsp/java-app.git', branch: 'master')
      }
    }
    stage('Maven build') {
      steps {
        bat(script: 'cd SpringMVCSecurityXML/ && mvn clean install -Dbuild.number', returnStatus: true, returnStdout: true)
      }
    }
  }
}