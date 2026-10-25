
pipeline {
    agent any

    stages {
        stage('Check JDK') {
            steps {
                bat 'java -version'
            }
        }

        stage('Validate Website') {
            steps {
                bat 'if not exist index.html exit /b 1'
                bat 'findstr /C:"CareerMatch" index.html'
            }
        }

        stage('Check Dockerfile') {
            steps {
                bat 'if not exist Dockerfile exit /b 1'
            }
        }

        stage('Build Complete') {
            steps {
                echo 'CareerMatch validation completed successfully!'
            }
        }
    }
}
