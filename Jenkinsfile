pipeline {
    agent any
    stages {
        stage ('Clean Stage') {
            steps {
                withMaven(maven : 'maven3.5') {
                    sh 'mvn clean'
                }
            }
        }
        stage ('Package Stage') {
            steps {
                withMaven(maven : 'maven3.5') {
                    sh 'mvn package'
                }
            }
        }
        stage ('Deploy Stop & Start') {
            steps {
                sh './deploy'
            }
        }
    }
}