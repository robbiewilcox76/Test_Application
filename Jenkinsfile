pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Run the Gradle build command
                    sh './gradlew build'
                }
            }
        }
    }
}
