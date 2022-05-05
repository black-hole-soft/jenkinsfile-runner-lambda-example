pipeline {
    agent any
    environment {
        PATH = "/usr/local/bin:$PATH"
    }
    stages {
        stage('Build') {
            steps {
                sh """
                git clone https://github.com/black-hole-soft/jenkinsfile-runner-lambda-example.git
                export JAVA_HOME=\$(/usr/libexec/java_home -v 1.8)
                mvn -Duser.home=/tmp clean package
                """
            }
        }
    }
}
