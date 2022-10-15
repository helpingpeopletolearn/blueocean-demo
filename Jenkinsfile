pipeline {
  agent any
  stages {
    stage('Install Apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Fetch code') {
      steps {
        git(url: 'git@github.com:helpingpeopletolearn/blueocean-demo.git', branch: 'main')
      }
    }

    stage('Deploy code') {
      steps {
        sh 'sudo cp -R . /var/www/html/'
      }
    }

  }
}