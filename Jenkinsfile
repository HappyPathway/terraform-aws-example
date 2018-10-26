pipeline {
  agent any
  stages {
    stage('TerraTest') {
      steps {
        sh '''cd test;
go test -v -run TestTerraformAwsExample'''
      }
    }
  }
  environment {
    GOPATH = '/var/lib/jenkins/go/'
    PATH = '/usr/lib/go-1.10/bin:${PATH}'
  }
}