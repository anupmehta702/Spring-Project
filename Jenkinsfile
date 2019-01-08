pipeline {
    agent any
    stages {
        stage('check enviornment') {
            steps {
               bat 'echo %PATH%'
            }
        }
        stage('build') {
            steps {
               bat 'mvn clean package install'
            }
        }
    }
}
