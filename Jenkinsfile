env.git_repo_name="git@github.com:balag91/jenkins-example" // update this value as created in Step 9 above
env.git_id="13bf12b1-5d6f-4203-801d-3bb2ef5b6c22"  

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
