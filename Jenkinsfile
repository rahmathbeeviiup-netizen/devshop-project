pipeline {
    agent any

    stages {

        stage('checkout') {
            steps {
                deleteDir()

                sh '''
                    git clone https://github.com/rahmathbeeviiup-netizen/devshop-project.git
                '''
            }
        }

        stage('deploy') {
            steps {
                sh '''
                    rm -rf /var/www/html/*
                    cp -r devshop-project/* /var/www/html/
                '''
            }
        }
    }
}
