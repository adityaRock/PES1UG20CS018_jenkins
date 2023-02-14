pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o pes1ug20cs010_task5 pes1ug20cs010_task5.cpp'
                build job: 'PES1UG20CS010-1'
            }
        }
        
        stage('Test') {
            steps {
                sh './pes1ug20cs010_task5'
            }
        }
        
        stage('Deploy') {
            steps {
                eco 'Deployment? idk'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
            }
            }
}
