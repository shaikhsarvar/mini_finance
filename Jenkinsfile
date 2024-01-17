pipeline {
    agent any

    stages {
        stage('Package') {
            steps {
                echo 'Building..'
                sh 'rm -rf /var/www/html/*'
            }
        }
        stage('Build') {
            steps {
                echo 'Building....'
                sh 'cp -r * /var/www/html'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying to jenkins public ip on port 80.'
            }
        }
    }
}
