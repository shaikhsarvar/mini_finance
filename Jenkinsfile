pipeline {
    agent any

    stages {
        stage('Git Scm') {
            steps {
                echo 'checkout to main'
                git branch: 'main', url: 'https://github.com/shaikhsarvar/mini_finance.git'
            }
        }

        stage('Clean up') {
            steps {
                echo 'clean up directory'
                sh 'rm -rf /var/www/html/*'
            }
        }

        stage('Build') {
            steps {
                echo 'building the app....'
                sh 'cp -r * /var/www/html/'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the app on jenkins public ip on port 80'
            }
        }
    }
}

