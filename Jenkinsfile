pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                withEnv(['HTTP_PROXY=http://PITC-Zscaler-Global-ZEN.proxy.corporate.ge.com:80']) {
                    sh 'npm install'
                }
            }
        }
    }
}
