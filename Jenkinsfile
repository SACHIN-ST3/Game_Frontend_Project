pipeline {

    agent any

    environment {
        SERVER = "ubuntu@18.209.50.67"
        TARGET = "/var/www/html"
    }

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Deploy') {

            steps {

                sshagent(credentials: ['nginx-ssh']) {

                    sh '''
                    ssh -o StrictHostKeyChecking=no $SERVER "rm -rf $TARGET/*"

                    scp -o StrictHostKeyChecking=no -r ./* $SERVER:$TARGET
                    '''
                }

            }

        }

    }

}
