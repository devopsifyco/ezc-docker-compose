pipeline {
    agent { docker { image 'node:20.11.0-alpine3.19' } }

    parameters {
        choice(name: 'APP', choices: ['test', "demo"], description: 'You could have other types of parameters besides choice.')
        choice(name: 'ENVIRONMENT', choices: ['test', "demo"], description: 'You could have other types of parameters besides choice.')
        string(name: 'VERSION', defaultValue: '', description: 'version of app to deploy')
    }
    stages {
        stage('build') {
            steps {
                sh 'node --version'
                print "${params.Release}\r\n"
                print "${params.ScanSonar}\r\n"
            }
        }
    }
}