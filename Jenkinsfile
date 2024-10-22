pipeline{
    agent any 
    stages{
        stage("checkout"){
            steps{
                checkout scm
            }
        }

        stage ("version check"){
            steps{
                sh "node --version"
                sh "npm --version"
            }
        }

        stage("Test"){
            steps{
                sh 'npm install'
                sh 'npm test'
            }
        }

        stage("Build"){
            steps{
                sh 'npm run build'
            }
        }
    }
}
