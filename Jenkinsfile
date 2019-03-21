pipeline {
    agent any	
	stages {
        stage('Initialize') {
            steps {
                bat '''
                    echo "PATH = %PATH%"
                    '''
                }
            }
	    stage('Build stage') {
		    steps {
			    withMaven(maven : 'maven_3_6_0' ) {
			}	    bat 'cd sudha-app && mvn build'
				}
		}
		
		stage('Testing Stage') {
		    steps {
			    withMaven(maven : 'maven_3_6_0' ) {
			}	    bat 'mvn test'
                }
		}
      	
		stage('Deloying stage') {
		    steps {
			    withMaven(maven : 'maven_3_6_0' ) {
			}	    bat 'mvn deploy'
                }
		}	    
	}	

}