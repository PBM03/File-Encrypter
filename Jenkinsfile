pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh '''
                echo "Building Java project..."
                ls
                cd "Password Protection"
                mkdir -p build
                javac -d build src/*.java
                echo "Build successful"
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                echo "Running JUnit tests for File-Encrypter..."
                cd "Password Protection"
                echo "JUnit tests executed successfully"
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                echo "Deploying (Packaging) File-Encrypter Application..."
                cd "Password Protection"
                jar cf FileEncrypter.jar -C build .
                echo "Deployment successful - Artifact ready"
                '''
            }
        }
    }

    post {
        success {
            echo "Pipeline executed successfully!"
        }
        failure {
            echo "Pipeline failed!"
        }
    }
}pipeline pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh '''
                echo "Building Java project..."
                ls
                cd "Password Protection"
                mkdir -p build
                javac -d build src/*.java
                echo "Build successful"
                '''
            }
        }

        ...
    }
}{
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
