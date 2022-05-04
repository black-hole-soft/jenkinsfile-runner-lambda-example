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
                git clone https://github.com/black-hole-soft/jenkinsfile-runner-lambda-example.git'
                echo 'Jerry Script'
                env
                echo $JAVA_HOME
                /usr/libexec/java_home -V
                ls /Library/Java/JavaVirtualMachines
                java -version
                #mvn -Duser.home=/tmp clean package'
                """
            }
        }
    }
}
