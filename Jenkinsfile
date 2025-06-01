pipeline{
    agent {label 'AGENT-1'}
    environment{
        PROJECT= "EXPENSE"
        COMPONENT= "BACKEND"
    }
    options{
        disableConcurrentBuilds()
        sleep 15
    }
    stages{
        stage('build'){
            steps{
                script{
                        sh """
                            echo "this is build"
                            echo "this is $PROJECT"
                         """   
                    }
                }
             } 
        stage ('test'){
            steps{
                script{
                        sh """
                            echo "this is test"
                        """    
                    }
                }
            } 
        stage ('deploy') {
            steps{
                script{
                    sh """
                        echo "this is deploy"
                     """

                }
            }

        }     
     }
     post {
        always{
            echo "I will always say hello again"
        }
        success {
            echo "I will always say hello again"
        }
        failure{
            echo "The pipeline has failed"
        }
     }

}        

        
    
