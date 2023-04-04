pipeline {
    agent any

    environment {
        ANDROID_HOME = "/usr/lib/android-sdk/platform-tools/"
        PATH = "$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools"
    }

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/prithvirajpowar/Demo.git']]])
            }
        }

        stage('Install dependencies') {
            steps {
                sh '''
                    cd your-flutter-project
                    flutter pub get
                '''
            }
        }

        stage('Run tests') {
            steps {
                sh '''
                    cd your-flutter-project
                    flutter test
                '''
            }
        }

        stage('Build APK') {
            steps {
                sh '''
                    cd your-flutter-project
                    flutter build apk --release
                '''
            }
        }

    }
}
