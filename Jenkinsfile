pipeline {
	agent any
              environment {
                         EXECUTE="TRUE"
                         }
              
                    stages {
		       stage('First') {
                
			       steps {
				    script {
                                           
                                            echo “Updating Second Stage”
					
				}
			}
                        }

                   stage('Second') {
 
                            when { 
                                    environment name: 'EXECUTE', value: 'True'
                                 }

			       steps {
				
					      echo $EXECUTE
                                     }

                        }
                    stage('Third') {
			     when { 
                                    environment name: 'EXECUTE', value:'False'
                                  } 

			steps {
				
					    echo "nothing to do"
					
			
			     }
                       }

        }
}

