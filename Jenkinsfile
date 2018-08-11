pipeline {
  agent any
  stages {
    stage('Print Env Vars') {
      environment {
        AWS_ACCESS_KEY_ID = credentials('AWS_ACCESS_KEY_ID')
        AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
      }
      steps {
        sh 'echo "Hello"'
        sh 'echo "AWS_ACCESS_KEY_ID = $AWS_ACCESS_KEY_ID"'
        sh 'echo "AWS_SECRET_ACCESS_KEY = $AWS_SECRET_ACCESS_KEY"'
      }
    }
  }
}
