pipeline
{
  agent any
     stages
     {
      stage('clone')
      {
          steps
          {
           git branch: 'main', credentialsId: 'dc48e0c8-238d-4edd-a31c-8be6f379668f', url: 'https://github.com/QANaveen/MavenScripttojenkins.git'
           }
      }
      stage('Build') 
       {
         steps
         {
           bat 'mvn -f C:\\Users\\User\\.jenkins\\workspace\\MavenScriptingithub\\Mavenpipeline\\pom.xml test package'
         }
       } 
       stage('report')
       {
         steps
         {
           junit 'Mavenpipeline\\target\\surefire-reports\\Test-*.xml'
         }
       }
   }
 }

