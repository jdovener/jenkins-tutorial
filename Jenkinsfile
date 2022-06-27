pipeline{
        agent any
        stages{
            stage('Clone Repo'){
                steps{
                    sh "git clone https://gitlab.com/qacdevops/chaperootodo_client"
                }
            }
            stage('Install Docker and Docker-compose'){
                steps{
                    sh "apt install docker docker-compose"
                }
            }
            stage('Deploy'){
                steps{
                    sh "sudo docker-compose pull && sudo -E DB_PASSWORD=${DB_PASSWORD} docker-compose up -d"
                }
            }
        }
}