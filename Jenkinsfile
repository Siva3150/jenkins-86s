pipeline {
    // These are pre-build section
    agent {
        node {
            label 'AGENT-1'
        }
    } 
    // This is build section
    stages{
        stage('Build'){
            steps {
                script {
                    """
                    echo "Building"

                    """
                }
            }
        }
        stage('Test'){
            steps{
                script{
                    """
                    echo "Testing"

                    """
                }
            }
        }
        stage('Deploy'){
            steps{
                script {
                    """
                    echo "Deplpying"

                    """
                }
            }
        }
    }
          // This is post-build section
        post{
            always{
                echo 'I will run always say Hello Again!'
            }
            success{
                echo 'I will run if pipeline success'
            }
            failure{
                echo 'I will run if pipeline failure'
            }
    }
}