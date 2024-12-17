pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    echo "Building the app...."
                    echo "Execute the branch $BRANCH_NAME"
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo "Testing the App...."
                }
            }
        }
        stage('Deploy') {
            when {
                expression {
                    BRANCH_NAME == 'main'
                }
            }
            steps {
                script {
                    echo "Deploying the App"
                }
            }
        }
    }
}
