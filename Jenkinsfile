pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS018_task5 PES1UG20CS018_task5.cpp'
                build job: 'PES1UG20CS018-1'
            }
        }
        
        stage('Test') {
            steps {
                sh './PES1UG20CS018_task5'
            }
        }
        
        stage('Deploy') {
            steps {
                eco 'Deployment'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
