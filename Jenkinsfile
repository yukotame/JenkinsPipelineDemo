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
                withCredentials(bindings: [sshUserPrivateKey(credentialsId: 'MySSH', \                                            
                                             passphraseVariable: 'yuko1124', \
                                             usernameVariable: 'sakitamefusa')]) {
  // some block
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
