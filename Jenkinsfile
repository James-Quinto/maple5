pipeline {
	agent any
	
	stages {
		stage("Connecting to Platforms") {
			steps {
				sh 'uname -a'
			}
		}
		
		stage("Deployment Test") {
			parallel {
				stage("Linux / Rhel") {
					steps {
						sh 'uname -a'
					}
				}
				stage("Linux / Debian") {
					steps {
						sh 'uname -a'
					}
				}
				stage("Windows Server") {
					steps {
				sh 'uname -a'
			}
		}
		
		stage("Deployment Test") {
			parallel {
				stage("Linux / Rhel") {
					steps {
						sh 'uname -a'
					}
				}
				stage("Linux / Debian") {
					steps {
						sh 'uname -a'
					}
				}
				stage("Windows Server") {
					steps {
						sh 'uname -a'
					}
				}
			}
		}
		
		stage("Deploy") {
			steps {
				echo "Deploy!"
			}
		}
	}
}
