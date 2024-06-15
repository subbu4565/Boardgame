pipeline {    
    agent {
        docker {
            image 'maven:3.9.7-amazoncorretto-11-debian-bookworm'
            
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
