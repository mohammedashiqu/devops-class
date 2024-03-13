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
        stage('Update image') {
            steps {
                sh '''
                echo $BUILD_NUMBER
                // rm -rf ./cd-prod-yamls
                // git clone https://ashiq-betaflux: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@github.com/nayan-tech/cd-prod-yamls.git 
                // ls cd-prod-yamls
                // sed -i 's|image: ${DOCKER_REPO2}:.*|image: ${DOCKER_REPO2}:${BUILD_NUMBER}|' ./cd-prod-yamls/c3-v2-kafka/deployment.yaml
                // cat ./cd-prod-yamls/c3-v2-kafka/deployment.yaml
                '''
            }
        }
    }
}

