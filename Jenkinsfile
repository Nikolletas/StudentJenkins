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
    }
}