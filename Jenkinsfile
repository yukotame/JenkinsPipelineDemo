pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello from GitHub hook trigger'
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying'
 withCredentials([usernamePassword(credentialsId: 'MySSH', passwordVariable: 'yuko1124', usernameVariable: 'sakitamefusa')]) {
        remote.user = sakitamefusa
        remote.password = yuko1124

        stage("SSH Steps Rocks!") {

        }
                
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing'
            }
        }
        
        stage('Release') {
            steps {
                echo 'Releasing'
            }
        }
    }
}
