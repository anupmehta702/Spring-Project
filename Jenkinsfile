pipeline {
   // agent { docker { image 'maven:3.3.3' } }
    docker { image 'node:7-alpine' }
   // agent any
    stages {
        stage('build') {
            steps {
                //sh 'mvn --version'
                bat "echo Hello World"
            }
        }
    }
}
