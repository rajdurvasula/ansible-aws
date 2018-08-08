pipeline {
  agent any
  stages {
    stage('Launch EC2 node') {
      steps {
        ansiblePlaybook(playbook: 'ec2_site.yml', disableHostKeyChecking: true, dynamicInventory: true)
      }
    }
  }
}