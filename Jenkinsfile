pipeline {
   agent any

   stages {
      
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