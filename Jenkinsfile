pipeline {
   agent any
      stages {
        stage('Source') {
		  
		  steps {
               git 'https://github.com/PrashantBastapure/Maven-Project.git'		  
		     }
			}
			
		stage('build') {	 
          
          steps {
		      sh 'mvn clean install'
		  }		  
		  
		}	
	  }
   }