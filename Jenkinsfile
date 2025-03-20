pipeline{
   agent {
      docker {
         image 'maven'
             }
         }
   stages{
      stage('check the vesion'){
        steps{
          bat 'mvn -version'
             }
         }
     }
post{
    success{
     echo "job is success"
     cleanWs()
  }
    failure{
    echo "job is failed"
   }
  }
}
