pipeline {
    agent any	
	stages {
	    stage('Build stage') {
		    steps {
			    withMaven(maven : 'M2_HOME' ) {
				    sh 'mvn -f /root/MavenProjects/simple-app/pom.xml clean compile'

					}
            }
		}
	}
}
