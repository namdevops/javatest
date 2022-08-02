pipeline {
    agent any
    tools {
        maven "maven"
    }
    stages {
        stage('Build') {
            steps {
                sh  'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                echo 'Test.'
            }
        }
        stage("code quality"){
            steps{
                echo "quality"
            }
        }       
         stage('Deploy to dev') {
            steps {
                echo 'Dev ....'
            }
        }
        stage('Deploy to test') {
            steps {
                echo 'test....'
            }
        }
        stage('Deploy to uat') {
            steps {
                echo 'UAT ....'
            }
        }
        stage('Deploy to pre production') {
            steps {
                echo 'staging '
                }
            }
        
        stage('Deploy to prod') {
            steps {
                echo 'prod ....'
            }
        }
    }
}