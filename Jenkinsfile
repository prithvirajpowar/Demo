pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/prithvirajpowar/Demo.git'
            }
        }
        
        stage('Build') {
            steps {
                sh 'flutter pub get'
                sh 'flutter build apk'
            }
        }
        
        stage('Archive APK') {
            steps {
                archiveArtifacts artifacts: 'build/app/outputs/apk/release/app-release.apk', fingerprint: true
            }
        }
    }
}
