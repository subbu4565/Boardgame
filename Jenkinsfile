pipeline {    
    agent {
        docker {
            image 'subbu4565/maven:java11'
            
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
