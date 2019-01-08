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
               bat(/"C:\Program Files\apache-maven-3.0.5\bin\mvn" clean package install/);
            }
        }
    }
}
