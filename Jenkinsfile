pipeline {
    agent any
    tools {
        maven "maven-3.9.2"
        jdk "JDK"
    }
    environment {
        JAVA_HOME = tool(name: 'JDK', type: 'jdk').getHome()
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
                dir("/home/gazal/.jenkins/workspace/demo1") {
                    sh 'mvn -B -DskipTests clean package'
                }
            }
        }
    }
}
