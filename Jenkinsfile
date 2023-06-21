pipeline {
    agent any
    tools {
        maven "maven-3.9.2"
        jdk "JDK"
    }
    stages {
        stage('Initialize') {
            steps {
                echo "PATH = ${M2_HOME}/bin:${PATH}"
                echo "M2_HOME = /opt/maven"
                echo "JAVA_HOME = ${JAVA_HOME}"
            }
        }
        stage('Build') {
            steps {
                echo "JAVA_HOME = ${JAVA_HOME}"
                dir("/home/gazal/.jenkins/workspace/demo1") {
                    echo "JAVA_HOME = ${JAVA_HOME}"
                        sh 'mvn clean'
                        sh 'mvn install'
                }
            }
        }
    }
}
