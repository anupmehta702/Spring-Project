pipeline {
    environment {
      mvnHome='echo %MAVEN_HOME%'
   }
    agent any
    stages {
        node {
          stage("Print variables") {
            def foo = "foo"
            bat "echo ${foo}"
          }
        }
        stage('check enviornment') {
            steps {
               bat 'echo %PATH%'   
            }
        }
        stage('build') {
            steps {
                echo mvnHome
               bat(/"%MAVEN_HOME%\bin\mvn" clean package install/);
            }
        }
    }
}
