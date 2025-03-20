pipeline{
   agent {
      docker {
         image 'naresh20/hello-world-python:0.0.1.Release'
         label 'my-defined-label'
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
