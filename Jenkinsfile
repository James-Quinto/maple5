pipeline {
	agent any
	
	stages {
		stage("Platform Checkout") {
			steps {
				sh 'mvn -v'
			}
		}
		
		stage("Agent Deployment Testing") {
			parallel {
				stage("Red Hat") {
					agent { docker 'openjdk:7-jdk-alpine' }
					steps {
						sh 'uname -a'
					}
				}
				stage("Ubuntu") {
					agent { docker 'openjdk:8-jdk-alpine' }
					steps {
						sh 'uname -a'
					}
				}
				stage("Windows") {
					steps {
						sh 'uname -a'
					}
				}
			}
		}
		
		stage("Performance Testing") {
			parallel {
				stage("Red Hat") {
					agent { docker 'openjdk:7-jdk-alpine' }
					steps {
						sh 'uname -a'
					}
				}
				stage("Ubuntu") {
					agent { docker 'openjdk:8-jdk-alpine' }
					steps {
						sh 'uname -a'
					}
				}
				stage("Windows") {
					steps {
						sh 'uname -a'
					}
				}
			}
		}
		stage("Notifying Slack") {
			steps {
				echo "Deploy!"
			}
		}
	}
}
