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
		   withMaven(jdk: 'JAVA_HOME', maven: 'MAVEN_HOME'){
	         	sh 'mvn clean compile'
			echo "this is compile stage"
		  }		  
		}
	      }
	      
	      stage('Test') {	 
                steps {
                   echo "this is Test stage"
		  }		  
		}	
	
        stage('build') {	 
           steps { 
		   withMaven(jdk: 'JAVA_HOME', maven: 'MAVEN_HOME'){
	         	sh 'mvn clean package'
			echo "this is build stage"
		  }		  
		}
	      }
	
	         
	 
	      
	      stage ('SSH Connection and Deploy'){
             steps {
			    sshagent(['tomcat']) {
                    sh 'scp -o StrictHostKeyChecking=no */target/*.war ec2-user@172.31.41.31:/var/lib/tomcat/webapps'
                          }
                 		}
					  }
		
	
	 }
   }
