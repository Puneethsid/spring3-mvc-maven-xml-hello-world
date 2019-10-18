node {
   def mvnHome
   stage('getscm') { // for display purposes
      // Get some code from a GitHub repository
      git credentialsId: '0d665a2d-e9c8-4c6d-8dad-b7ebb7f62053', url: 'https://github.com/Puneethsid/spring3-mvc-maven-xml-hello-world.git'
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
      mvnHome = tool 'maven'
   }
   stage('Build') {
      // Run the maven build
      if (isUnix()) {
         sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
      } else {
      echo 'this is build maven artifact'
         bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
      }
   }
   stage ('deploy'){
   echo 'deployment started'
       bat '''copy C:\\Users\\punes\\.jenkins\\workspace\\Spring-helloword-pipeline\\target\\*.war C:\\Users\\punes\\Downloads\\apache-tomcat-8.5.46-windows-x64\\apache-tomcat-8.5.46\\webapps'''
   }  
   
}
