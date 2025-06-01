pipeline{
    agent any
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
}        

        
    
