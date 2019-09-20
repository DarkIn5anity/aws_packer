pipeline {
    agent any

    environment {
        AWS_ACCESS_KEY_ID     = "${env.AWS_ACCESS_KEY_ID}"
        AWS_SECRET_ACCESS_KEY = "${env.AWS_SECRET_ACCESS_KEY}"
    }

    stages {
        stage('Plan') {
            steps {
                script {
                    currentBuild.displayName = "${version}"
                }
                sh '/usr/local/bin/packer build ubuntu.json'
            }
        }
    }
}