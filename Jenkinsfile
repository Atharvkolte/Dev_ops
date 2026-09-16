pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
            }
        }

        stage('Build') {
            steps {
                echo 'Compiling Java program...'
                sh 'javac HelloJenkins.java'
            }
        }

        stage('Run') {
            steps {
                echo 'Running Java program...'
                sh 'java HelloJenkins'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
