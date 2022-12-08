pipeline {
	agent any
                stages {
		       stage('First') {
                
			       steps {
				    script {
                                             environment {
						EXECUTE="True"
                                             }
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
				
					    echo “nothing to do”
					
			
			     }
                       }

        }
}

