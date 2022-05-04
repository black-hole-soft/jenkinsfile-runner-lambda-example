pipeline {
    agent any
    environment {
        PATH = "/usr/local/bin:$PATH"
        JAVA_HOME = "/Library/Java/JavaVirtualMachines/jdk1.8.0_331.jdk/Contents/Home"
    }
    stages {
        stage('Build') {
            steps {
                sh """
                git clone https://github.com/black-hole-soft/jenkinsfile-runner-lambda-example.git
                export JAVA_HOME=\$(/usr/libexec/java_home -v 1.8)
                java -version
                mvn -version
                mvn -Duser.home=/tmp clean package
                """
            }
        }
    }
}
