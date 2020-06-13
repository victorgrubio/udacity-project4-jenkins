pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-east-1', credentials:'f7c109df-d22d-410c-a868-345dcfb6acb4') {
                    def identity=awsIdentity(); //Log AWS credentials
                    // Upload files from working directory 'dist' in your project workspace
                    s3Upload(file:'index.html', bucket:'jenkins-udacity-victorgrubio', path:'/index.html')
                }
            }
        }   
    }
}