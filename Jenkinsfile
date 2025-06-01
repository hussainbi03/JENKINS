pipeline{
    agent {label 'AGENT-1'}
    environment{
        PROJECT= "EXPENSE"
        COMPONENT= "BACKEND"
        DEPLOY_TO= "production"
    }
    options{
        disableConcurrentBuilds()
        timeout(time: 5, unit: 'MINUTES')
    }
     parameters{
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: 'JENKINS', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages{
        stage('build'){
            steps{
                script{
                        sh """
                            echo "this is build"
                            echo "this is $PROJECT"
                            echo "hello, ${params.PERSON}"
                            echo "hell0 ${params.BIOGRAPHY}"
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
            input{
                message "should we continue"
                ok "yes, we should"
                submitter "shabbu"
            }
            when {
                environment name: 'DEPLOY_TO', value: 'production'
            }
            steps{
                script{
                    sh """
                        echo "this is deploy"
                        sleep 15
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

        
    
