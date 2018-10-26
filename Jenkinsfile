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
  environment {
    GOPATH = '/var/lib/jenkins/go/'
    PATH = '/usr/lib/go-1.10/bin:${PATH}'
  }
}