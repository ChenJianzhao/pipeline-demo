#!groovy
pipeline {
    agent any
    stages {
        stage('Non-Parallel Stage') {
            steps {
                echo 'This stage will be executed first.'
            }
        }
        stage('Parallel Stage') {
            when {
                branch 'master'
            }
            failFast true
            stages {
                stage('Nested 1') {
                    steps {
                        echo "In stage Nested 1 within Branch C"
                    }
                }
                stage('Nested 2') {
                    steps {
                        echo "In stage Nested 2 within Branch C"
                    }
                }
            }
        }
    }
}