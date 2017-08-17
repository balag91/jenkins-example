pipeline {
    agent { node { label 'Slave' } }
    #tools {
        #maven 'M3' 
    #}
	stages {
	    stage ('compiling stage') {
		
		   steps {
			       sh 'mvn compile'
		   }
		}
		
		stage ('Testing stage') {
		
		   steps {
			       sh 'mvn test'
		   }
		}
		
	}
	}
