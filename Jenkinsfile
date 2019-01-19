pipeline {
    //agent { docker { image 'ceddy4395/windows-java' } }
    //agent { docker { image 'maven:3-alpine' } }
   // agent { docker { image 'node:7-alpine' } }
    //agent { docker { image 'openjdk' } }
    agent { docker { openjdk:8-jdk-alpine' } } 
   // agent any
    stages {
        stage('build') {
            steps {
                sh 'java --version'
                //bat "echo Hello World"
               //bat "docker info"
            }
        }
    }
}
