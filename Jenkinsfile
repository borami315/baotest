pipeline {
  agent any
  stages {
    stage('Clone Git Repository') {
      steps {
        git url: 'https://github.com/borami315/baotest.git', branch: 'main'
      }
    }
    
    stage('Run Ansible Playbook') {
      steps {
        sh '''                        
        ansible-playbook ./playbook.yml
        '''
      }
    }
  }
}
