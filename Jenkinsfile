pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from Git repository...'
                git branch: 'main', url: 'https://github.com/FawadUlHassan/simpleweb.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies... (placeholder for now)'
                // In real-world scenarios, you would install software or dependencies here.
            }
        }
        stage('Static Analysis') {
            steps {
                echo 'Running HTML linting...'
                sh 'tidy -q -e index.html cta.html || true' // Example of running an HTML linter
            }
        }
        stage('Build') {
            steps {
                echo 'Building the website...'
                sh 'echo "Building complete."'
            }
        }
        stage('Test') {
            steps {
                echo 'Running basic tests...'
                // Placeholder: Include test commands if applicable
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying to web server...'
                sh 'sudo cp -r * /var/www/html'
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}

