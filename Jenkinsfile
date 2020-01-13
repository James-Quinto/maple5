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
            }
        }
    }
}
          
                        
