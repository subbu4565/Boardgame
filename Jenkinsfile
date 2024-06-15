pipeline {    
    agent {
        docker {
            image 'maven:3.2.3-jdk-8-onbuild'
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
