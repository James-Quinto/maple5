pipeline {
	agent any
	
	stages {
		stage("Platform Checkout") {
			steps {
				sh 'uname -a'
			}
		}
		
		stage("Agent Deployment Test") {
			parallel {
				stage("Oracle RAC") {
					steps {
						sh 'uname -a'
					}
				}
				stage("SQL Cluster") {
					steps {
						sh 'uname -a'
					}
				}

			}
		}
		
		stage("Performance Test") {
			parallel {
				stage("Oracle RAC") {
					steps {
						sh 'uname -a'
					}
				}
				stage("SQL Cluster") {
					steps {
						sh 'uname -a'
					}
				}

			}
		}
		
		stage("Ratt-Tool Test") {
			parallel {
				stage("Oracle RAC") {
					steps {
						sh 'uname -a'
					}
				}
				stage("SQL Cluster") {
					steps {
						sh 'uname -a'
					}
				}

			}
		}
		
		stage("Generating Reports") {
			parallel {
				stage("WCF Reports") {
					steps {
						sh 'uname -a'
					}
				}
				stage("Diagnostic Reports") {
					steps {
						sh 'uname -a'
					}
				}
			}
		}
		
		stage("Notifying Slack") {
			steps {
				echo "Build Finished!"
			}
		}
	}
}
