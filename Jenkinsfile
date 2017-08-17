pipeline {
    agent { node { label 'Slave' } }
	
	stages {
	    stage ('compiling stage') {
		
		   steps {
		       withMaven(maven : 'M3') {
			       sh 'mvn compile'
			   }
		   }
		}
		
		stage ('Testing stage') {
		
		   steps {
		       withMaven(maven : 'M3') {
			       sh 'mvn test'
			   }
		   }
		}
		
	}
	}
