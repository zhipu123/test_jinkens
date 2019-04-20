pipeline {
    agent {docker 'node:11-alpine'}
    stages{
        stage('Build'){
            steps{
                echo 'Building'
            }
        }
        stage('Test'){
            steps{
                echo 'Testing'
                sh "node index.js"

            }
        }

        stage('Deploy-Production'){
            input{
                message "Should we continue?"
                ok "Yes, we should."
            }
            steps{
                echo 'Deploy-Production!'

            }
        }
    }
}
