pipeline{
    agent any
    }
    stages{
        stage("build"){
            steps{
            sh mvn deploy
            }
        }
            stage("docker build")
            {
              steps{ 
                  sh docker build -t nischala17/Docker-Project:latest .
                      }
            }
            stage("docker push") 
            {
                steps {
           sh docker push nischala17/docker-project:latest
            }
            }
            stage("remove image")
            {
                steps{
           sh docker rmi nischala17/docker-project:latest
            }
            }
            stage("all images")
            {
             sh steps{  docker images
                   }
            }
    }
