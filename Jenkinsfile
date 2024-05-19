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
            dir("jenkin-maven-demo"){
                sh "mvn clean install -Dmaven.test.skip=true"
            } 
        }
     }
     stage("run"){
        steps {
            dir("jenkin-maven-demo/target"){
                sh "java -jar maven-jenkins-demo-0.0.1-SNAPSHOT.jar"
            } 
        }
     }
   }
}