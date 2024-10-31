pipeline {
  agent any
  stages {
    stage('Deploy Docker Image on Master') {
        git url: 'https://github.com/borami315/baotest.git', branch: 'main'
      }
      steps {
        sh '''
        ansible-playbook ./playbook.yml
        '''
      }
    }
  }
}
