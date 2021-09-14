pipeline
{
  agent any
  {
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
           mvn -f 
         }
       }
      post
      {
         junit 'test-results.xml' 
     
     }
   }
 }
