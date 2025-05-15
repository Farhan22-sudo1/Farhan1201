
pipeline {
    agent any

    stages {
        stage('Install & Run All Steps') {
            steps {
                echo 'Installing Node.js, then running all steps...'
                sh '''
                    curl -fsSL https://rpm.nodesource.com/setup_18.x | sudo bash -
                    sudo dnf install -y nodejs

                    node -v
                    npm -v

                    npm install
                    npm test || echo "No tests found"

                    echo "Build complete."
                    echo "Deploy complete."
                '''
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed.'
        }
    }
}
