pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Kaniha4/24MIS0398_Assessment7_P2.git'
            }
        }

        stage('Build') {
            steps {
                bat 'javac StudentManagement.java'
            }
        }

        stage('Archive Artifact') {
            steps {
                archiveArtifacts artifacts: 'StudentManagement.class', fingerprint: true
            }
        }
    }
}
