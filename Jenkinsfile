pipeline pipeline {
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
