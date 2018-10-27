pipeline {
  agent any
  stages {
    stage('TerraTest') {
      steps {
        sh '''#!/bin/bash
cd test;
source ~/vault.sh
AWS_CREDENTIALS=$(vault read aws/creds/ec2_admin --format=json)
export AWS_ACCESS_KEY_ID=$(echo ${AWS_CREDENTIALS} | jq .data.access_key)
export AWS_SECRET_ACCESS_KEY=$(echo ${AWS_CREDENTIALS} | jq .data.secret_key)
export PATH=/usr/lib/go-1.10/bin/:${PATH}
go test -v -run TestTerraformAwsExample'''
      }
    }
  }
  environment {
    GOPATH = '/var/lib/jenkins/go/'
    PATH = '/usr/lib/go-1.10/bin:${PATH}'
    AWS_DEFAULT_REGION = 'us-east-1'
  }
}