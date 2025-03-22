
pipeline
    agent any

    stages{
        stage('clone repository') {
            steps {
                git  branch: 'main', url: 'https://github.com/Saitejabatti/Finalproject.git'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "building the application"'
            }
        }

        stage('deploy to s3') {
            steps {
                script {
                    echo 'Deploying to S3...'
                    sh 'aws s3 sync . s3://mystaticwebsites3/ --delete'
                }
            }
        }
    }
