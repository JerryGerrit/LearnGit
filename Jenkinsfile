pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        sh 'echo "This is Jenkins Blue Ocean"'
      }
    }
    stage('error') {
      steps {
        sh 'ls'
      }
    }
    stage('triggerOther') {
      steps {
        build 'testjob'
      }
    }
    stage('send mail') {
      steps {
        emailext(subject: 'test', body: 'this is blue ocean test mail', to: 'zhiye.feng@samsung.com')
      }
    }
  }
}