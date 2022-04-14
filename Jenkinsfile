pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'pwd && ls -la'
                sh 'git https://github.com/feyzee/jenkins-helm-integration-workshop workshop'
                dir('workshop') {
                    sh 'pwd && ls -la'
                }
                /* dir('workshop') { */
                /*     sh 'helm package .' */
                /* } */
            }
        }
        /* stage('Deploy') { */
        /*     steps { */
        /*         dir('workshop') { */
        /*             sh 'helm install assign-helm-0.1.0.tgz --generate-name' */
        /*         } */
        /*     } */
        /* } */
    }
}
