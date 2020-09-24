pipeline {
   agent any
      stages {
        stage('Source') {
	    steps {
               echo "this is source stage"
		  }
		}
			
	stage('build') {	 
           steps {
	    	   echo "this is build stage"
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
