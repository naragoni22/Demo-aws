pipeline{
   agent any
   stages{
      stage('mvn install'){
        steps{
          sh 'mvn clean install'
             }
         }
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
