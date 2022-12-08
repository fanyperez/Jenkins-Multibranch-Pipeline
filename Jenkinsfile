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
                                    EXECUTE="True"
                                 }

			       steps {
				
					      echo $EXECUTE
                                     }

                        }
                    stage('Third') {
			     when { 
                                    EXECUTE="False"
                                  } 

			steps {
				
					    echo “nothing to do”
					
			
			     }
                       }

        }
}

