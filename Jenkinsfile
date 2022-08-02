pipeline {
    agent any
    tools {
        maven " maven"
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
                echo 'staging ....
                }
            }
        post {
            always {
                echo 'One way or another, I have finished'
                deleteDir() /* clean up our workspace */
        }
        success {
            echo 'I succeeded!'
        }
        unstable {
            echo 'I am unstable :/'
        }
        failure {
            mail to: 'team@example.com',
             subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
             body: "Something is wrong with ${env.BUILD_URL}"
        }
        changed {
            echo 'Things were different before...'
        }
    }

        stage('Deploy to prod') {
            steps {
                echo 'prod ....'
            }
        }
    }
}