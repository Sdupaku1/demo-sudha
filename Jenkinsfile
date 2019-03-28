pipeline {
    agent any	
	stages {
	    stage('Build stage') {
		    steps {
			    withMaven(maven : 'M2_HOME' ) {
				    dir('/root/MavenProjects/simple-app/src/main/java/com/home/app')
				    sh 'mvn clean compile'

					}
            }
		}
	}
}
