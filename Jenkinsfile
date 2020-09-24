pipeline {
   agent any
      stages {
        stage('Source') {
	    steps {
               git 'https://github.com/PrashantBastapure/Maven-Project.git'
			  echo "this is source stage"
		  }
		}
			
	stage('build') {	 
           steps {
	      sh 'mvn clean install'
		   echo "this is build stage"
		  }		  
		}	
	      
	stage('Test') {	 
           steps {
              echo "this is Test stage"
		  }		  
		}	
	  }
   }
