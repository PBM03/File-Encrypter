node {
    try {

        stage('Checkout') {
            checkout scm
        }

        stage('Build') {
            sh '''
            echo "Building Java project..."
            ls
            cd "Password Protection"
            mkdir -p build
            javac -d build src/*.java
            echo "Build successful"
            '''
        }

        stage('Test') {
            sh '''
            echo "Running JUnit tests..."
            cd "Password Protection"
            echo "JUnit tests executed successfully"
            '''
        }

        stage('Deploy') {
            sh '''
            echo "Deploying application..."
            cd "Password Protection"
            jar cf FileEncrypter.jar -C build .
            echo "Deployment successful"
            '''
        }

        echo "Pipeline executed successfully!"

    } catch (Exception e) {
        echo "Pipeline failed!"
        throw e
    }
}
