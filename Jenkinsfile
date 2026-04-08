pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo "Building project..."
                sh 'javac App.java'
            }
        }

        stage('Test') {
            steps {
                echo "Running project..."
                sh 'java App'
            }
        }

        stage('Archive') {
            steps {
                echo "Saving artifact..."
                archiveArtifacts artifacts: '*.class', fingerprint: true
            }
        }
    }
}
