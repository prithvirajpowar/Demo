pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/prithvirajpowar/flutter-project.git'
            }
        }
        
        stage('Build') {
            steps {
                sh 'flutter packages get'
                sh 'flutter build apk --licenses'
            }
        }
    }
}
