pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                echo "📥 Pulling code from GitHub..."
                checkout scm
            }
        }

        stage('Deploy to Server') {
            steps {
                echo "🚀 Running deployment script..."
                sh 'bash /var/lib/jenkins/deploy.sh'
            }
        }
    }

    post {
        success {
            echo "✅ Deployment completed successfully!"
        }
        failure {
            echo "❌ Deployment failed!"
        }
    }
}
