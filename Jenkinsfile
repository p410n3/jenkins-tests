pipeline {
    agent any

    environment {
        XFPATH = '/var/www/xf'
    }
    
    stages {
        stage('Building Release') {
            steps {
                sh 'ls /xd'
            }
        }
    }
    post {
        success {
          echo 'Client is Deployed'
        }
        failure {
          echo 'This will run only if failed'
        }
        changed {
          echo 'Client Status of Build changed'
        }
    }
}
