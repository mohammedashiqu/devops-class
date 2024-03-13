pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Check out code from the Git repository
                sh "ls"
            }
        }

        stage('Build') {
            steps {
                // Build the Java project (replace 'mvn clean install' with your build command)
                echo "mvn clean install"
            }
        }

        stage('Test') {
            steps {
                // Run tests (replace with your test commands)
                echo "mvn test"
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the application (replace with your deployment commands)
                // For example, you could deploy to a web server, Docker registry, etc.
                echo "scp target/myapp.jar user@server:/path/to/deployment/directory"
            }
        }
    }
}

