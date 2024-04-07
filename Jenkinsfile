pipeline {
  agent any
  stages {
    stage('Fetch Code') {
      steps {
        git(branch: 'main', url: 'https://github.com/x4teen/jenkins-test.git')
      }
    }

    stage('Install Apache') {
      steps {
        sh 'sudo yum install httpd -y'
        sh 'sudo systemctl start httpd'
      }
    }

    stage('Deploy App') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}