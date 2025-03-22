pipeline {
    agent any  // ✅ Make sure this is correctly written
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Saitejabatti/Finalproject.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the application...'
            }
        }
        stage('Deploy to S3') {
            steps {
                sh 'aws s3 sync . s3://mystaticwebsites3 --delete'
            }
        }
    }
}

