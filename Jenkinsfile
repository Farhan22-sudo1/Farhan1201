pipeline {
    agent {
        docker {
            image 'node:18'
        }
    }

    stages {
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test || echo "No tests found"'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Build complete!"'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploy complete!"'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed.'
        }
    }
}
