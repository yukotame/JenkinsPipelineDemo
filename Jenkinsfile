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
                def remote = [:]
                remote.name = 'sakitamefusa'
                remote.host = 'localhost'
                remote.user = 'sakitamefusa'
                remote.password = 'yuko1124'
                remote.allowAnyHosts = true
                stage('Remote SSH') {
                      sshCommand remote: remote, command: "ls -lrt"
                      sshCommand remote: remote, command: "for i in {1..5}; do echo -n \"Loop \$i \"; date ; sleep 1; done"
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
