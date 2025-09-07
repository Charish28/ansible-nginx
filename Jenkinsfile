pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps { checkout scm }
    }
    stage('Run Ansible') {
      steps {
        sh '''
          ansible --version
          ansible-playbook -i inventory.ini nginx-playbook.yml
        '''
      }
    }
  }
}
