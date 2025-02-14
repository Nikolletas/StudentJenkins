pipeline{
    agent any
    stages{
        stage('NPM Install'){
            steps{
                bat 'npm install'
            }  
        }
        stage('Run audit tests'){
            steps{
                bat 'npm audit'
            }   
        }
        stage('Run integration tests'){
            steps{
                bat 'npm run test'
            }
        }
        stage('Deploy to STAGING'){
            steps{
                echo 'Deploying to staging'
            }
        }
        stage('Approval for Production Deployment') {
            steps{
                script {
                    input message: 'Procced with production deployment?', ok: 'Deploy'
                }
            }
        }
        stage('Deploy to PRODUCTION'){
            steps{
                echo 'Deploy to production'
            }
        }
    }
}