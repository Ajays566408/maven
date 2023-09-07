@Library('cicd')_
pipeline
{
    agent any
    stages
    {
        stage('ContDownload_loans')
        {
            steps
            {
                script
                {
                    codes.gitDownload("my_maven")
                    
                }
            }
        }
        
        stage('ContBuild_loans')
        {
            steps
            {
                script
                {
                    codes.newBuild()
                    
                }
            }
         }	
      } 
}







                  











                    










               



        
        


