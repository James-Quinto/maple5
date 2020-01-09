ppipeline {
  agent any
  stages {
  stage('DSA upgraded from DSM') {
      steps {
        script { //sh './SlackNotifA.sh'
          echo 'Sending Notification to Slack'
        }
      }
    }
  stage('Test:Installation') {
      steps {
        script { //sh './jenkins/Pwett.sh'
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
  stage('Test:Diagnostic') {
      steps {
        script { //sh './Diag.sh'
          echo 'Running Diagnostic Checking'
        }
      }
    }
  stage('Collection:Reports and Log') {
      steps {
        script { //sh './Collector'
          echo 'Collecting Log and Uploading to WCF'
        }
      }
    }
  }
}
