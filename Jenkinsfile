pipeline {
    agent { docker { image 'node:20.11.0-alpine3.19' } }
    parameters {
        booleanParam name: 'Release', defaultValue: false, description: 'Build release version'
        booleanParam name: 'ScanSonar', defaultValue: false, description: 'Scan Sonarqube for CodeQuality'
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