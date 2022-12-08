pipeline {
	agent any
            stages {
		STAGE 1 
                
			steps {
				script {
                                             environment {
						EXECUTE="True"
                                             }
                                             echo “Updating Second Stage”
					
				}
			}

                STAGE 2 
                      when { 
                           EXECUTE="True"
                       }

			steps {
				
						echo $EXECUTE
					
			
			}

                STAGE 3 
			when { 
                           EXECUTE="False"
                       }

			steps {
				
						echo “nothing to do”
					
			
			}
                       }

}

