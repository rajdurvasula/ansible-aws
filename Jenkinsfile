pipeline {
  agent any
  stages {
    stage('Launch EC2 node') {
      steps {
        ansiblePlaybook(playbook: 'ec2_site.yml', disableHostKeyChecking: true, dynamicInventory: true, extras: '-e ec2_operation=launch_instance -e instance_name=Springboot_Test1')
      }
    }
  }
}