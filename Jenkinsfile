pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES2UG22CS394 abc.cpp'  
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './PES2UG22CS394' 
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
