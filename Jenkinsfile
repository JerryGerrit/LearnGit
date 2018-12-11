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
  }
}