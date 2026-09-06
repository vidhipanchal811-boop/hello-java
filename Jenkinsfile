pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/vidhipanchal811-boop/hello-java.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }

    post {
        success {
            echo 'Pipeline Succeeded'
        }

        failure {
            echo 'Pipeline Failed'
        }
    }
}
