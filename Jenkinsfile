pipeline {
    agent any
    environment {
        PATH = "/usr/local/bin:$PATH"
        JAVA_HOME = '/opt/usr/lib/jvm/java-openjdk'
    }
    stages {
        stage('Build') {
            steps {
                sh """
                git clone https://github.com/black-hole-soft/jenkinsfile-runner-lambda-example.git
                export JAVA_HOME=$(/usr/libexec/java_home -v 1.8)
                java -version
                mvn -version
                mvn -Duser.home=/tmp clean package
                """
            }
        }
    }
}
