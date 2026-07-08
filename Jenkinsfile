pipeline {

    agent any

    environment {
        SERVER = "ubuntu@18.209.50.67"
    }

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Deploy') {
            steps {
                sshagent(credentials: ['nginx-ssh']) {
                    sh '''
                    rsync -avz --delete \
                    -e "ssh -o StrictHostKeyChecking=no" \
                    dist/ $SERVER:/tmp/website/

                    ssh -o StrictHostKeyChecking=no $SERVER "
                        sudo rm -rf /var/www/html/*
                        sudo cp -r /tmp/website/* /var/www/html/
                    "
                    '''
                }
            }
        }

    }
}
