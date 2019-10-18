pipeline {
    agent any
    stages {
       

        stage ('Build') {
            steps {
                 bat 'mvn clean package'
            }
        }
		
		 stage ('Deploy') {
            steps {
               bat '''copy C:\\Users\\punes\\.jenkins\\workspace\\build1\\target\\*.war C:\\Users\\punes\\Downloads\\apache-tomcat-8.5.46-windows-x64\\apache-tomcat-8.5.46\\webapps'''
            }
        }
    }
}
