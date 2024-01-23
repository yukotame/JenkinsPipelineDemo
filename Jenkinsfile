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

                sshagent(credentials: ['MySSH']) 
                {
                    sh 'pwd' 
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
