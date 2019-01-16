pipeline {
    //agent { docker { image 'ceddy4395/windows-java' } }
    //agent { docker { image 'maven:3.3.3' } }
   // agent { docker { image 'node:7-alpine' } }
    agent { docker { image 'openjdk' } }
   // agent any
    stages {
        stage('build') {
            steps {
                sh 'java --version'
                bat "echo Hello World"
               bat "docker info"
            }
        }
    }
}
