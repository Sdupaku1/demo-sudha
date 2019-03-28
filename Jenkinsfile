pipeline {
    agent any	
	stages {
	    stage('Build stage') {
		    steps {
			    withMaven(maven : 'M2_HOME' ) {
				    dir('simple-app/src/main/java/com/home/app')
				    sh 'mvn clean compile'

					}
            }
		}
	}
}
