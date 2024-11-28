pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                // Add your build command here, e.g., './build.sh'
                sh './build.sh'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your test command here, e.g., './run_tests.sh'
                sh './run_tests.sh'
            }
        }
        stage('Deploy') {
            when {
                branch 'main'
            }
            steps {
                echo 'Deploying to production...'
                // Add your deploy command here, e.g., './deploy.sh'
                sh './deploy.sh'
            }
        }
    }
}
