pipeline {
    agent any

    environment {
        FLUTTER_HOME = tool 'flutter'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Setup') {
            steps {
                sh "${FLUTTER_HOME}/bin/flutter config --no-analytics"
                sh "${FLUTTER_HOME}/bin/flutter doctor -v"
            }
        }
        stage('Build') {
            steps {
                sh "${FLUTTER_HOME}/bin/flutter pub get"
                sh "${FLUTTER_HOME}/bin/flutter build apk --split-per-abi"
            }
        }
        stage('Test') {
            steps {
                sh "${FLUTTER_HOME}/bin/flutter test"
            }
        }
    }
}
