pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from GitHub...'
                git branch: 'main', url: 'https://github.com/FawadUlHassan/simpleweb.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the website...'
                // For static sites, this step is optional unless there's a build process (e.g., minifying files)
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your test commands here if needed. For now, we’ll just echo.
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the website...'
                // Replace this with your deployment strategy
                // For example, copying files to /var/www/html:
                sh 'cp -r * /var/www/html'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed.'
        }
        success {
            echo 'Pipeline succeeded.'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}

