pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'sh ehco "Hello World"'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'yum install -y httpd'
            sh 'sudo systemctl start httpd'
          }
        }

        stage('test-1') {
          steps {
            sh 'ls -al'
          }
        }

      }
    }

  }
}