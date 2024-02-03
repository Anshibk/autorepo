pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Clean workspace before checkout
                    deleteDir()

                    // Clone the repository and specify the branch
                    checkout([$class: 'GitSCM', branches: [[name: 'main']], userRemoteConfigs: [[url: 'https://github.com/Anshibk/autorepo.git']]])
                }
            }
        }

        stage('Build and Deploy') {
            steps {
                // Your build and deploy steps here
                echo 'Build and deploy steps go here'
                sh 'echo asd | sudo -S cp index.html /var/www/html/'
                sh "ls /var/www/html/"
            }
        }
    }
}
