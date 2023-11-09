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
                  docker build -t nischala17/docker-project:$tag_value .
                      }
            }
            stage("docker push") 
            {
                steps {
            docker push nischala17/docker-project:$tag_value
            }
            }
            stage("remove image")
            {
                steps{
            docker rmi nischala17/docker-project:$tag_value
            }
            }
            stage("all images")
            {
              steps{  docker images
                   }
            }
    }
