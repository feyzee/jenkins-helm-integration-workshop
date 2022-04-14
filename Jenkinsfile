pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                git 'https://github.com/feyzee/jenkins-helm-integration-workshop'
                dir('jenkins-helm-integration-workshop') {
                    sh 'pwd && ls -la'
                    sh 'helm package .'
                }
            }
        }
        stage('Deploy') {
            steps {
                dir('workshop') {
                    sh 'helm install assign-helm-0.1.0.tgz --generate-name'
                }
            }
        }
    }
}
