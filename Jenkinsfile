pipeline{
    agent any
    }
    stages{
        stage("build"){
            steps{
            sh 'mvn install'
            }
        }
            stage("docker build")
            {
              steps{ 
                  sh 'docker build -t nischala17/docker-project:latest .'
                      }
            }
            stage("docker push") 
            {
                steps {
           sh 'docker push nischala17/docker-project:latest'
            }
            }
            stage("remove image")
            {
                steps{
           sh 'docker rmi nischala17/docker-project:latest'
            }
            }
            stage("all images")
            {
             steps{ 
                 sh 'docker images'
                   }
            }
    }
