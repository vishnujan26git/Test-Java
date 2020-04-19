pipeline {
   agent any

   stages {
       
      stage('Checkout') {
         steps {
            git credentialsId: 'e53ee257-df96-41b6-888d-ac8e6972af52', url: 'https://github.com/vishnujan26git/Test-Java.git'
         }
      }
      
      stage('Build JAR & Execute') {
         steps {
            bat label: '', script: '''cd src
            javac RunProgram.java
            jar -cfe Helloworld.jar RunProgram *.class
            java -jar Helloworld.jar'''
         }
      }
   }
}