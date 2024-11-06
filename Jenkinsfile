pipeline {
  agent any
  stages {
    # Git 저장소 복사
    stage('Clone Git Repository') {
      steps {
        git url: 'https://github.com/wonjune95/jenkinstest.git', branch: 'main'
      }
    }
    stage('Deploy Docker Image on Master') {
      environment {
        ANSIBLE_HOST_KEY_CHECKING = 'False'   
        ANSIBLE_PRIVATE_KEY_FILE = '/var/lib/jenkins/.ssh/ansible_key'  
      }
      steps {
        sh '''                        
        ansible-playbook ./playbook.yml
        '''
      }
    }
  }
}
