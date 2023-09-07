@Library('cicd')_
pipeline
{
    agent any
    stages
    {
        stage('ContDownload_master')
        {
            steps
            {
                script
                {
                    codes.gitDownload("my_maven")
                    
                }
            }
        }
        
        stage('ContBuild_master')
        {
            steps
            {
                script
                {
                    codes.newBuild()
                    
                }
            }
        }
        stage('ContDeployment_master')
        {
            steps
            {
                script
                {
                    codes.newDeployment("DeclarativePipelineWithSharedLibraries","172.31.34.55","testapp3")
                    
                }
            }
        }
        stage('ContTesting_master')
        {
            steps
            {
                script
                {
                    codes.gitDownload("FuncTesting")
                    codes.runSelenium("DeclarativePipelineWithSharedLibraries")
                    
                }
            }
        }
        stage('ContDelivery_master')
        {
            steps
            {
                script
                {
                    codes.newDeployment("DeclarativePipelineWithSharedLibraries","172.31.42.174","prodapp3")
                    
                }
            }
        }
        
        
    }
}
