pipeline {
  agent any
  stages {
    stage('Deploy Docker Image on Master') {  
      steps {
        git url: 'https://github.com/borami315/baotest.git', branch: 'main'
        sh '''
          ansible-playbook ./playbook.yml
        '''
      }
    }
  }
}
