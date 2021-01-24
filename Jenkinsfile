pipeline{
 agent any
 stages{
   stage("code checkout"){
   steps{
     git(credentialsId: 'Github', url: 'https://github.com/vamsi0047/sonar-example.git')
     }
   }
   stage("build the code"){
     steps{
      echo "=============== Excuting the tests========="
      sh " mvn clean test"
     }
     }
   stage("publishing test reports"){
     steps{
        echo "========= Excuting Test Reports==========="
       junit '**/surefire-reports/*.xml'
     }
   }
   }
 }

