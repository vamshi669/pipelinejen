pipeline {
    agent {
        label 'dev'
    }

    stages {
        stage('BUILD') {
            steps {
                echo 'This is Build stage'
                sh '''
                    sleep 5
                    echo "Build completed successfully"
                '''
            }
        }

        stage('TEST PARALLEL') {
            parallel {
                stage('test on chrome') {
                    steps {
                        echo 'This is Test stage on chrome browser'
                        sh 'sleep 5; exit 1'
                    }
                }
                stage('test on edge') {
                    steps {
                        echo 'This is Test stage on microsoft edge'
                        sh 'sleep 5; exit 1'
                    }
                }
            }
        }
        stage('DEPLOY') {
            steps {
                echo 'This is Deploy stage'
                sh '''
                    sleep 5
                    echo "Deployment completed successfully"
                '''
            }
        }
    }
}
