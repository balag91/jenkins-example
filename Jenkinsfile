pipeline {
    agent { node { label 'Slave' } }
    //tools {
        //maven 'M3' 
    //}
	stages {
	    stage ('compiling stage') {
		
		   steps {
			       sh 'mvn compile'
		   }
		}
		
		stage ('Packaging stage') {
		
		   steps {
			       sh 'mvn package'
			   }
		   }
		stage ('Installation stage') {
		
		   steps {
			       sh 'mvn install'
			   }
		   }
		
		stage ('Testing stage') {
		
		   steps {
			       sh 'mvn test'
		   }
		}
		
	}
	}
