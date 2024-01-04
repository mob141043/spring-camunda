pipeline {

    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
            post {
                always {
                    echo 'Test done.'
                }
            }
        }

        stage('Deliver') {
            steps {
                echo 'Deliver successfully.'
            }
        }
    }
}