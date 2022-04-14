pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                git clone 'https://github.com/feyzee/jenkins-helm-integration-workshop' workshop
                cd workshop
                helm package .
            }
        }
        stage('Deploy') {
            steps {
                cd workshop
                helm install assign-helm-0.1.0.tgz --generate-name
            }
        }
    }
}
