pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    sh 'git clone https://github.com/robbiewilcox76/Test_Application.git'
                    sh 'cd Test_Application && git checkout master'  // or 'main' if needed
                }
            }
        }
    }
}
