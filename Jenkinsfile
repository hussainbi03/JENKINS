pipeline{
    agent {label 'AGENT-1'}
    stages{
        stage('build'){
            steps{
                script{
                        sh """
                            echo "this is build"
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

        
    
