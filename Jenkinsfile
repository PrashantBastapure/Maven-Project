pipeline {
   agent any
      stages {
        stage('Source') {
	    steps {
	       git 'https://github.com/PrashantBastapure/Maven-Project.git'	    
               echo "this is source stage"
		  }
		}
			
	stage('Compile') {	 
           steps { 
		   withMaven(MAVEN_HOME: 'MAVEN_HOME'){
	         	sh 'mvn clean compile'
			echo "this is compile stage"
		  }		  
		}
	      }
	
        stage('build') {	 
           steps { 
		   withMaven(MAVEN_HOME: 'MAVEN_HOME'){
	         	sh 'mvn clean install'
			echo "this is build stage"
		  }		  
		}
	      }
	
	stage('Test') {	 
           steps {
              echo "this is Test stage"
		  }		  
		}	
	      
	 stage('Approval') {	 
           steps {
	      input 'get approval'	   
              echo "this is Approval stage stage"
		  }		  
		}	
	  }
   }
