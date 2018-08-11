pipeline {
  agent any
  environment {
    AWS_ACCESS_KEY_ID = credentials('AWS_ACCESS_KEY_ID')
    AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
    ROOT_PWD = credentials('root_password_of_this_vm')
  }
  stages {
    stage('Run Ansible') {
      steps {
        ansiblePlaybook(
          playbook: 'ec2_site.yml',
          colorized: true,
          disableHostKeyChecking: true,
          dynamicInventory: true,
          extras: '-e ec2_operation=launch_instance -e instance_name=Springboot_Test1 -e ansible_become_pass=$ROOT_PWD')
      }
    }
  }
}
