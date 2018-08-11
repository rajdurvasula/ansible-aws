pipeline {
  agent any
  stages {
    stage('Get AWS Access Key') {
      steps {
        input(message: 'AWS access key', id: 'aws_access_key_id', ok: 'String', submitter: 'aws_access_key', submitterParameter: 'aws_access_key_param')
      }
    }
    stage('Get AWS Secret Key') {
      steps {
        input(message: 'AWS secret key', id: 'aws_secret_key', ok: 'String', submitter: 'aws_secret_key', submitterParameter: 'aws_secret_key_param')
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