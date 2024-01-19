pipeline {
    agent { docker { image 'node:20.11.0-alpine3.19' } }
    parameters {
        choice(name: 'APP', choices: ['BackEnd', "FronEnd-Android","Database"], description: 'You could have other types of parameters besides choice.')
        choice(name: 'ENVIRONMENT', choices: ['test', "demo"], description: 'You could have other types of parameters besides choice.')
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