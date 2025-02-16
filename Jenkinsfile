pipeline {
    agent any
    environment {
        ANDROID_HOME = '/opt/android-sdk'
        PATH = "$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools"
    }

    stages {
        stage('Build') {
            steps {
                // Clean and build the Gradle project
                sh './gradlew clean build'
            }
        }
    }

    post {
        always {
            // Archive the build artifacts
            archiveArtifacts artifacts: 'build/libs/*.jar', allowEmptyArchive: true
        }
        success {
            echo 'Build succeeded!'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
