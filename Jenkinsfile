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
        timeout(time:10, unit:'MINUTES')
        disableConcurrentBuilds()

    }
    parameters {
    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
    booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
    choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
    password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    // This is build section
    stages{
        stage('Build'){
            steps {
                script {
                    """
                    echo "Building"
                    echo $COURSE
                    sleep 10
                    env

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