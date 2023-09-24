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
                sh "echo Build step git"
            }
        }
        stage('Test'){
            steps{
                sh 'echo Test step git'
            }
        }
        stage('Deploy')
        {
            steps{
                sh "echo Deploy step git"
            }
        }
        stage('Stage 5'){
            steps{
                sh "echo Stage 5 step git"
            }
        }
    }
}
