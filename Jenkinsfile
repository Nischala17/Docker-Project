pipeline{
    agent any
    }
    stages{
        stage("build"){
            steps{
             mvn deploy
            }
        }
            stage("docker build")
            {
              steps{ 
                  docker build -t nischala17/docker-project:latest .
                      }
            }
            stage("docker push") 
            {
                steps {
            docker push nischala17/docker-project:latest
            }
            }
            stage("remove image")
            {
                steps{
            docker rmi nischala17/docker-project:latest
            }
            }
            stage("all images")
            {
              steps{  docker images
                   }
            }
    }
