pipeline{
   agent any
   stages{
     stage("clean up"){
        steps {
            deleteDir()
        }
     }
     stage("clone"){
        steps {
            sh "git clone https://github.com/sathishkumar-developer/jenkin-maven-demo.git"
        }
     }
     stage("build"){
        steps {
            sh "mvn clean install"
        }
     }
     stage("test"){
        steps {
            sh "mvn test"
        }
     }
   }
}