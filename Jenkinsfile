pipeline {
    agent any	
	stages {
	    stage('Build stage') {
		    steps {
			    withMaven(maven : 'M2_HOME' ) {
				    dir('sudha-app')
				    sh 'mvn clean compile'

					}
            }
		}
	}
}
