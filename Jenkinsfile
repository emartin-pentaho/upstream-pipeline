pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build the software!'
        script {
          publishEvent jsonEvent('{"eventName":"buildCompleted", "SUITE_RELEASE_VERSION":"8.3.0.0"}'), verbose: true
        }
      }
    }
    stage('Testing') {
      steps {
        sh 'sleep 2'
        sh 'echo Tests Completed!'
        script {
          publishEvent jsonEvent('{"eventName":"testCompleted", "SUITE_RELEASE_VERSION":"8.3.0.0"}'), verbose: true
        }
      }
    }
  }
}