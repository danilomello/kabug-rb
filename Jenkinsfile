pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building or resolving dependencies'
                sh 'bundle install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running regressions tests'
                
            }
        }

        stage('UAT') {
            steps {
                echo 'Waiting for user acceptance'
                input(message: 'Go to production?', ok:'Yes')
            }
        }

        stage('Prod') {
            steps {
                echo 'WebApp is ready'
            }
        }
    }
}