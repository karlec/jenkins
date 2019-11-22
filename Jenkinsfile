pipeline {
    agent any
    stages{
        stage("Checkout GIT"){
            steps{
                echo "====++++executing Checkout GIT+++===="
                git poll: true, 'https://github.com/karlec/jenkins.git' 
            }
            post{
                always{
                    echo "====++++always++++===="
                }
                success{
                    echo "====++++Checkout GITexecuted succesfully++++===="
                }
                failure{
                    echo "====++++Checkout GITexecution failed++++===="
                }
        
            }
            stage("Ls "){
                steps{
                    echo "====++++executing A++++===="
                    sh '''
                        bash -c "ls /"
                        '''
                }
                post{
                    always{
                        echo "====++++always++++===="
                    }
                    success{
                        echo "====++++A executed succesfully++++===="
                    }
                    failure{
                        echo "====++++A execution failed++++===="
                    }
            
                }
            }
        }
    }
}