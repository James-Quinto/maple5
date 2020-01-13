pipeline {
  agent any
  stages {
  stage('DSA upgraded from DSM') {
    parallel {
      stage('Test On Windows') {
      steps {
        script { //sh './SlackNotifA.sh'
          echo 'Sending Notification to Slack'
        }
      }
    }
  stage('Test:Installation') {
      steps {
        script { sh 'sudo /jenkins/Pwett.sh'
          echo 'Running Deployment Checking'
        }
      }
    }
  stage('Test:Performance') {
      steps {
        script { //sh './Perf.sh'
          echo 'Running Performance Checking'
        }
      }
    }
  stage('Test:Network Engine') {
      steps {
        script { //sh './Ratt_test.sh'
          echo 'Running Diagnostic Checking'
        }
      }
    }
  stage('Collecting Log and Uploading to WCF') {
      steps {
        script { //sh './Collector'
          echo 'Collecting Log and Uploading to WCF'
        }
      }
    }
  }
}
