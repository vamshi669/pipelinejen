pipeline {
    agent {
        label 'dev'
    }

    stages {

        stage('BUILD') {
            steps {
                echo "This is Build stage"
                sh '''
                    sleep 5
                    echo "Build completed successfully"
                '''
            }
        }

        stage('TEST') {
            steps {
                echo "This is Test stage"
                sh '''
                    sleep 5
                    echo "Tests passed successfully"
                '''
            }
        }

        stage('DEPLOY') {
            steps {
                echo "This is Deploy stage"
                sh '''
                    sleep 5
                    echo "Deployment completed successfully"
                '''
            }
        }
    }
}
