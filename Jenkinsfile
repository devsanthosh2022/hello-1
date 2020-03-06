pipeline {
   agent any

   stages {
      stage('SCM Git clone') {
         steps {
            // Get some code from a GitHub repository
            git 'https://github.com/nimmnisanthosh/hello-1.git'

         }

      }
      stage('SCM Maven build') {
          steps {
               // Run Maven on a Unix agent.
            sh "/opt/maven/bin/mvn clean package"

            // To run Maven on a Windows agent, use
            // bat "mvn -Dmaven.test.failure.ignore=true clean package"
          }
      }
   }
}

