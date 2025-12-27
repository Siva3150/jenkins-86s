pipeline {
    // These are pre-build sections
    agent {
        node {
            label 'AGENT-1'
        }
    }
     // This is build section
     stages{
        stage('Build'){
            steps{
             echo "Building"
            }
        }
        stage('Test'){
            steps{
                echo "Testing"
            }
        }
        stage('Deploy'){
            steps{
                echo "Deploying"
            }
        }
     }
     post {
        always{
            echo 'I will always say Hello again!'
        }
     }
}