pipeline {
    agent { node { label 'master' } }
	    // assigning slave nodes here.
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
		                 step([$class: 'ArtifactArchiver', artifacts: '**/target/*.jar', fingerprint: true])
                                 step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.xml'])
		   }
		}
	    }
	}
