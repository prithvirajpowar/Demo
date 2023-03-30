pipeline {
    agent any

    stages {
        stage('TEST') {
            steps {
                sh 'flutter test'
            }
        }
        stage('BUILD') {
            steps {
                sh 'flutter build apk --debug'
            }
        }
    }
}
