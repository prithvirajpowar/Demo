pipeline {
    agent any
    tools {
        flutter 'flutter'
    }
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/your-username/your-flutter-app.git'
            }
        }
        stage('Build APK') {
            steps {
                sh 'flutter build apk'
            }
        }
    }
}
