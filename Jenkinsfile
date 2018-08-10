#!groovy
pipeline {
    agent any
    stages {
        stage('Non-Sequential Stage') {
            agent {
                label 'for-non-sequential'
            }
            steps {
                echo "On Non-Sequential Stage"
            }
        }
        stage('Sequential') {
            environment {
                FOR_SEQUENTIAL = "some-value"
            }
            stages {
               stage('In Sequential 1') {
                   steps {
                       echo "In Sequential 1"
                   }
               }
               stage('In Sequential 2') {
                   steps {
                       echo "In Sequential 2"
                   }
               }
            }
        }
    }
}