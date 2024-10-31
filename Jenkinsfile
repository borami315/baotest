pipeline {
  agent any
  stages {
    stage('Deploy Docker Image on Master') {
        git url: 'https://github.com/beomtaek78/jenkinstest.git', branch: 'main'
      }
      steps {
        sh '''
        ansible-playbook ./playbook.yml
        '''
      }
    }
  }
}
