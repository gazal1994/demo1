pipeline {
    agent any
    tools {
        maven "maven-3.9.2"
        jdk "JDK"
    }
    stages {
        stage('Initialize') {
            environment {
                env.JAVA_HOME = /usr/lib/jvm/java-11-openjdk-amd64/bin/java
            }
            steps {
                echo "PATH = ${M2_HOME}/bin:${PATH}"
                echo "M2_HOME = /opt/maven"
                echo "JAVA_HOME = ${JAVA_HOME}"
            }
        }
        stage('Build') {
            steps {
                dir("/home/gazal/.jenkins/workspace/demo1") {
                    withEnv(["JAVA_HOME=${JAVA_HOME}"]) {
                        sh 'mvn -B -DskipTests clean package'
                    }
                }
            }
        }
    }
}
