pipeline {
    agent any

    environment{
        my_tag = "my_tag"
        my_name = "fsilvapucci"
    }
     
    

    stages{
        stage('Build'){
            steps{
                bat 'mvn clean package'
                bat "docker build . -t ${my_name}tomcatwebapp:${env.BUILD_ID}"
                bat "echo ${my_tag}"
            }

        }
    }
}