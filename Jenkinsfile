pipeline {
    agent any
    tools {
        maven "maven-3.9.2"
        jdk "JDK"
    }
    environment {
        JAVA_HOME = "/usr/lib/jvm/java-11-openjdk-amd64/bin/java"
    }
    stages {
        stage('Initialize'){
            steps{
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
   //  post {
   //     always {
   //        junit(
   //      allowEmptyResults: true,
   //      testResults: '*/test-reports/.xml'
   //    )
   //    }
   // } 
}
