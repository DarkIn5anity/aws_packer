pipeline {
    
    environment {
        AWS_ACCESS_KEY_ID     = "${env.AWS_ACCESS_KEY_ID}"
        AWS_SECRET_ACCESS_KEY = "${env.AWS_SECRET_ACCESS_KEY}"
    }
    agent {
        docker { image 'hashicorp/packer' }
    }

    stages {
        stage('Test') {
            steps {
                sh 'packer version'
            }
        }
    }
}