pipeline {
    agent any
    tools {
        maven "maven-3.9.2"
        jdk "JDK"
    }
    stages {
        stage('Initialize'){
            steps{
                echo "PATH = ${M2_HOME}/bin:${PATH}"
                echo "M2_HOME = /opt/maven"
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
