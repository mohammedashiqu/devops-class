pipeline {
    agent any
    environment {
        DOCKER_REPO1 = "gcr.io/nayandevops/qa-kafka_secured_layers-c3-v2-web"
        DOCKER_REPO2 = "gcr.io/nayandevops/qa-kafka_secured_layers-c3-v2-kafka"
        DOCKER_REPO3 = "gcr.io/nayandevops/qa-kafka_secured_layers-c3-v2-scheduler"
        doError = '0'
        BUILD_USER = ''
        eksc3_config = credentials('EKS-c3-v2-prod-recovered') 
    }

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
        stage('Update image') {
            steps {
                sh '''
                echo $BUILD_NUMBER
                echo hey $DOCKER_REPO3
                '''
            }
        }
    }
}

