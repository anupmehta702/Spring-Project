
node {
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
             stage("Print variables") {
                def foo = "foo"
                bat "echo ${foo}"
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
}
