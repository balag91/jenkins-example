pipeline {
    agent { node { label 'Slave' } }
	
	stages {
	    stage ('compiling stage') {
		
		   steps {
		       maven(maven : 'M3') {
			       sh 'mvn compile'
			   }
		   }
		}
		
		stage ('Testing stage') {
		
		   steps {
		       maven(maven : 'M3') {
			       sh 'mvn test'
			   }
		   }
		}
		
	}
	}
