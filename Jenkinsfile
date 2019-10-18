pipeline {
    agent any
    tools { 
        maven 'maven' 
        jdk 'JDK8' 
    }
    stages {
       

        stage ('Build') {
            steps {
                 bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
            }
        }
		
		 stage ('Deploy') {
            steps {
               bat '''copy C:\\Users\\punes\\.jenkins\\workspace\\build1\\target\\*.war C:\\Users\\punes\\Downloads\\apache-tomcat-8.5.46-windows-x64\\apache-tomcat-8.5.46\\webapps'''
            }
        }
    }
}
