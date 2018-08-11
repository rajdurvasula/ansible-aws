pipeline {
  agent any
  stages {
    stage('Get AWS Access Key') {
      steps {
        input(message: 'AWS access key', id: 'aws_access_key_id')
      }
    }
    stage('Get AWS Secret Key') {
      steps {
        input(message: 'AWS secret key', id: 'aws_secret_key')
      }
    }
    stage('Print keys') {
      steps {
        sh '''echo "AWS Secret Key = ${aws_secret_key}"
echo "AWS Access Key = ${aws_access_key}"'''
      }
    }
  }
}