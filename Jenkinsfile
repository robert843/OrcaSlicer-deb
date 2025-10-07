pipeline {
    agent {
        label 'java11'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Building project..."
                sh 'sleep 2' // tu wstaw build, np. `mvn package` albo `make`
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                sh 'sleep 2' // tu wstaw testy, np. `pytest` lub `npm test`
            }
        }
    }

    post {
        success {
            githubNotify context: 'jenkins/build', status: 'SUCCESS', description: 'Build passed!'
        }
        failure {
            githubNotify context: 'jenkins/build', status: 'FAILURE', description: 'Build failed!'
        }
        always {
            echo 'Build finished.'
        }
    }
}
