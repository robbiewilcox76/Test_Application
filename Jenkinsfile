pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from the repository
                git url: 'https://your-repo-url.git', branch: 'main'
            }
        }

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
