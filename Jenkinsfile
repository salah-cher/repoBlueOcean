pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello'
      }
    }
    stage('Validate') {
      steps {
        sh 'echo "ALL GOOD"'
      }
    }
    stage('OSVer') {
      steps {
        ansiblePlaybook(playbook: 'osver.yml', become: true, becomeUser: 'lnxcfg', colorized: true, disableHostKeyChecking: true, inventory: 'hosts')
      }
    }
  }
}