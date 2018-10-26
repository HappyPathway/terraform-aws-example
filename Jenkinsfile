pipeline {
  agent any
  stages {
    stage('') {
      steps {
        sh '''cd test;
dep ensure;
go test -v -run TestTerraformAwsExample;'''
      }
    }
  }
}