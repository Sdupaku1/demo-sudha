pipeline {
    agent any	
	stages {
	    stage('compile-Package stage') {
		    steps {
			    withMaven(maven : 'M2_HOME' ) {
				    sh 'mvn -f /root/MavenProjects/simple-app/pom.xml clean package'
					archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true

					}
				}
			}
		stage('Archive') {
			steps {
				withMaven(maven : 'M2_HOME' ) {
					sh 'mvn -f /root/MavenProjects/simple-app/pom.xml tomcat7:deploy'
					
				}
			}
		}
	}
}
