pipeline {
   agent any
   
   parameters{
       booleanParam(name: 'userFlag', defaultValue: true, description: '')
    }


   stages {
      
      stage('Build JAR & Execute') {
         steps {
         	
         	echo "flag set as : ${params.userFlag}"
			echo "***********************************"
            bat label: '', script: '''cd src
            javac RunProgram.java
            jar -cfe Helloworld.jar RunProgram *.class
            java -jar Helloworld.jar'''
         }
      }
   }
}