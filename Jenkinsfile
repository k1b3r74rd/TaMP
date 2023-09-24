pipeline{
    agent any
    stages{
        node('ubuntu'){
            def app
            stage('Cloning git'){
                steps{
                    checkout scm
                }
            }
            stage('Build'){
                steps{
                    sh "echo Build step git"
                    app = docker.build("kibertard/tamp")
                }
            }
            stage('Post-to-dockerhub'){
                steps{
                    sh 'echo Post-to-dockerhub'
                    docker.withRegistry("https://registry.hub.docker.com","dockerhub_creds"){
                        app.push("latest")}
                }
            }
            stage('Pull-image-server')
            {
                steps{
                    sh "echo Pull-image-server"
                    sh "docker-compose down"
                    sh "docker-compose up -d"
                }
            }
        }
    }
}
