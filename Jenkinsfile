pipeline {
  agent any
  stages {
    stage('Print Env Vars') {
      environment {
        AWS_ACCESS_KEY_ID = credentials('AWS_ACCESS_KEY_ID')
        AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
      }
      steps {
        /bin/bash ansible-playbook ec2_site.yml -e ec2_operations=launch_instance -e instance_name=Springboot_Test
      }
    }
  }
}
