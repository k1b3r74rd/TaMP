node('app'){
    def app
    stage('Cloning git'){
            checkout scm
    }
    stage('Build'){
            sh "echo Build step git"
            app = docker.build("kibertard/tamp")
    }
    stage('Post-to-dockerhub'){
            sh 'echo Post-to-dockerhub'
            docker.withRegistry("https://registry.hub.docker.com","dockerhub_creds"){
                app.push("latest")}
    }
    stage('Pull-image-server')
    {
            sh "echo Pull-image-server"
            sh "docker-compose down"
            sh "docker-compose up -d"
    }
}

