pipeline {
    agent any
    environment {
        NAME = 'VAM'
    }

    stages {
        stage('BUILD') {
            steps {
                echo "$NAME"
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
            parallel {
                stage('SERVER 1') {
                    steps {
                        echo 'This is Deploy to server1'
                        sh 'sleep 5'
                    }
                }
                stage('SERVER 2') {
                    steps {
                        echo 'This is Deploy to server2'
                        sh 'sleep 5'
                    }
                }

                stage('SERVER 3') {
                    steps {
                        echo 'This is Deploy to server3'
                        sh 'sleep 5'
                    }
                }
            }
        }
    }
}
