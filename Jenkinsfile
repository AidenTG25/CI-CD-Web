pipeline{
    agent any
    stages{
        stage('Clone Repository'){
            steps{
                git branch: 'main', url: "https://github.com/AidenTG25/CI-CD-Web.git"

            }
        }
        stage('Build Docker Image'){
            steps{
                bat 'docker build -t web-devops .'
            }
        }
        stage('Run Docker Container'){
            steps{
                bat 'docker run -d -p 8080:80 --name web-container web-devops'
            }
        }
    }
}