pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        sh '''cd test;
/var/lib/jenkins/go/bin/dep ensure;
go test -v -run TestTerraformAwsExample;'''
      }
    }
  }
}