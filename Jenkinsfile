pipeline {
	agent any
              
                    stages {
		       stage('First') {
                
			       steps {
				    script {
                                           
                                           env.EXECUTE="True"
                                           } 
                                            
					
				}
			}
                        }

                   stage('Second') {
 
                            when { 
                                    environment name: 'EXECUTE', value: 'True'
                                 }

			       steps {
				
                                              echo "Updating Second Stage"
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

