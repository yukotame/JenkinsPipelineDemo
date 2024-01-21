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
                sshagent(['jenkins']) {
                      sh 'scp  /var/lib/jenkins/workspace/JenkinsPipeline  sakitamefusa@localhost:/home/app_saki/test-env-jenkins'
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
