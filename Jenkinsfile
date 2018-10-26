pipeline {
  agent any
  stages {
    stage('TerraTest') {
      steps {
        sh '''cd test;
/var/lib/jenkins/go/bin/dep ensure;'''
      }
    }
  }
}