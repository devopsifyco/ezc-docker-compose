pipeline {
    agent { docker { image 'node:20.11.0-alpine3.19' } }
    parameters {
        string(name: 'APP', defaultValue: '', description: 'app to deploy')
        string(name: 'ENVIRONMENT', defaultValue: '', description: 'environment of app to deploy')
        string(name: 'VERSION', defaultValue: '', description: 'version of app to deploy')
    }
    stages {
        stage('build') {
            steps {
                sh 'node --version'
                echo "${params.ENVIRONMENT}:${params.APP} v${params.VERSION}\r\n"
            }
        }
    }
}