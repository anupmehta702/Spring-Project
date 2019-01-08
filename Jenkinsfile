pipeline {
    environment {
      mvnHome='echo %MAVEN_HOME%'
   }
    agent any
    stages {
        stage('check enviornment') {
            steps {
               bat 'echo %PATH%'   
            }
        }
        stage('build') {
            steps {
                echo mvnHome
               bat(/"${mvnHome}\bin\mvn" clean package install/);
            }
        }
    }
}
