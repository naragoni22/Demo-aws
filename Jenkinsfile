pipeline{
   agent any
   stages{
      stage('check the vesion'){
        steps{
          sh 'mvn -version'
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
