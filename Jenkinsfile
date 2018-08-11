pipeline {
  agent any
  stages {
    stage('Print Env Vars') {
      environment {
        AWS_ACCESS_KEY_ID = credentials('AWS_ACCESS_KEY_ID')
        AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
      }
      steps {
          ansiblePlaybook(
            playbook: 'ec2_site.yml',
            colorized: true,
            disableHostKeyChecking: true,
            dynamicInventory: true,
            extras: '-e ec2_operation=launch_instance -e instance_name=Springboot_Test1')
      }
    }
  }
}
