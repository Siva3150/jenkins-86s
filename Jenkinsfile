pipeline {
    // These are pre-build section
    agent {
        node {
            label 'AGENT-1'
        }
    } 
    environment {
        COURSE = "Jenkins"
    }
    options {
        timeout(time:10, unit:'SECONDS')
        disableConcurrentBuilds()

    }
    // This is build section
    stages{
        stage('Build'){
            steps {
                script {
                    """
                    echo "Building"
                    echo $COURSE
                    sleep 100

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
                cleanWs()
            }
            success{
                echo 'I will run if pipeline success'
            }
            failure{
                echo 'I will run if pipeline failure'
            }
            aborted{
                echo 'Pipeline is aborted'
            }
    }
}