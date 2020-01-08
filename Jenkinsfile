pipeline {
         agent any
         stages {
                 stage('Trigger Run A') {
                 steps {
                     sh './SlackNotifA.sh'
                 }
                 }
                 stage('Test:Installation') {
                 steps {
                    sh './Pwett.sh'
                 }
                 }
                 stage('Test:Performance') {
                 steps {
                    sh './Perf.sh'
                 }
                 }					
                 stage('Test:Diagnostic') {
                 steps {
                    sh './Diags.sh'
                 }
                 }
                 stage('Report') {
                 parallel { 
                            stage('Upgrade Reports') {
                           steps {
                                sh './ReportA.sh'"
                           }
                           }			 
                            stage('Upgrade Reports') {
                           steps {
                                sh './ReportB.sh'"
                           }
              }
}
}
