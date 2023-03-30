pipeline {
    agent any

    stages {
        stage('GIT PULL') {
            steps {
                git branch: "develop", url: 'https://github.com/prithvirajpowar/Demo.git'
            }
        }
        stage('TEST') {
            steps {
                sh 'flutter test'
            }
        }
        stage('BUILD') {
            steps {
                sh '''
                  #!/bin/sh
                  flutter build apk --debug
                  '''
            }
        }
    }
}
