pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build the software!'
        script {
          publishEvent event:jsonEvent('{"eventName":"buildCompleted", "SUITE_RELEASE_VERSION":"8.3.0.0"}'), verbose: true
        }
      }
    }
    stage('Testing') {
      steps {
        sh 'sleep 2'
        sh 'echo Tests Completed!'
        script {
          publishEvent event:jsonEvent('{"eventName":"testCompleted", "SUITE_RELEASE_VERSION":"8.3.0.0"}'), verbose: true
        }
      }
    }
  }
}