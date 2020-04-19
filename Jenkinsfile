pipeline {
   agent any
   parameters {
       	string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: 'Vishnu KP. No words to describe. A simple but yet powerful. Awesome!', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
   }
   stages {
      
      stage('Build JAR & Execute') {
         steps {
            bat label: '', script: '''cd src
            javac RunProgram.java
            jar -cfe Helloworld.jar RunProgram *.class
            java -jar Helloworld.jar'''
         }
      }
      
      stage('Example') {
            steps {
                echo "Hello ${params.PERSON}"
                echo "Biography: ${params.BIOGRAPHY}"
                echo "Toggle: ${params.TOGGLE}"
                echo "Choice: ${params.CHOICE}"
                echo "Password: ${params.PASSWORD}"
            }
         }
   }
}