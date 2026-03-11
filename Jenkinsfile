pipeline {
    agent any

    environment {
        AWS_DEFAULT_REGION = 'ap-south-1'
        S3_BUCKET = 'amz-s3-0111'
    }

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main',
                url: 'https://github.com/saurabh633848-max/website11.git'
            }
        }

        stage('Upload Files to S3') {
            steps {
                sh 'aws s3 sync . s3://$S3_BUCKET'
            }
        }

    }
}
