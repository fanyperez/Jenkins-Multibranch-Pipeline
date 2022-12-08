pipeline {
        agent any
                stages {
                       stage('First') {

                               steps {
                                      echo "step one"
                                    script {
                                            
                                                env.EXECUTE="True"

                                }
                        }
                        }

                   stage('Second') {

                            when {
                                    environment name: 'EXECUTE', value: 'True'
                                 }

                                steps { 
                                         echo "Updating Second Stage" 
                                      }

                                     script {

                                              echo ${EXECUTE}
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

