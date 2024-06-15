pipeline {    
    agent {
        docker {
            image 'adoptopenjdk/openjdk11'
            args '--user root -v /var/run/docker.sock:/var/run/docker.sock'
        }
    }

    stages {   
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        
        stage('Build') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
