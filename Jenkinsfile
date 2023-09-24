pipeline{
    agent any
    stages{
        stage('Cloning git'){
            steps{
                checkout scm
            }
        }

        stage('Build'){
            steps{
                sh "Build step git"
            }
        }
        stage('Test'){
            steps{
                sh 'Test step git'
            }
        }
        stage('Deploy')
        {
            steps{
                sh "Deploy step git"
            }
        }
        stage('Stage 5'){
            steps{
                sh "Stage 5 step git"
            }
        }
    }
}
