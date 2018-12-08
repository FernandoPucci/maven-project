pipeline {
    agent any

    environment{
        my_tag = "my_tag"
        my_name = "fsilvapucci"
    }
     
    

    stages{
        stage('Build'){
            steps{
                sh 'mvn clean package -X'
                sh "docker build . -t ${my_name}tomcatwebapp:${env.BUILD_ID}"
                sh "echo ${my_tag}"
            }

        }
    }
}