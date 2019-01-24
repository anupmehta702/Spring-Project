pipeline {
    environment {
        mvnHome = 'echo %MAVEN_HOME%'
    }
    agent any
    stages {
        stage('check enviornment') {
            steps {
                bat 'echo %PATH%'
            }
        }
        stage("Print variables") {
            steps{
                script{
                    def foo = "foo"
                    bat "echo ${foo}"
                }
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('build') {
            steps {
                bat(/"%MAVEN_HOME%\bin\mvn" clean package install/);
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}

