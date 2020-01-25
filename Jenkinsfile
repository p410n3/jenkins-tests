pipeline {
    agent any

    environment {
        XFPATH = '/var/www/xf'
    }
    
    stages {
        stage('Deployment') {
            steps {
                sh 'cp -r ./* $XFPATH/src/addons/jenkins/test/'
                 sh 'php $XFPATH/cmd.php xf-addon:upgrade jenkins/test'
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
