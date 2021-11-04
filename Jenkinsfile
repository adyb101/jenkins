pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo "Hello World"'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'sudo yum install -y httpd'
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