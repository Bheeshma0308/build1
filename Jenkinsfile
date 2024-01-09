pipeline
{
    agent any
    environment 
    {
        MAVEN_GOALS = 'clean install'        // Define the Maven goals for building the project  
    }
    stages
    {
        
        stage('Build')
        {
            steps
            {
                 sh "mvn ${MAVEN_GOALS}"
            }
        }
    }
    post
    {
        success
        {
            echo "Build successful!"
        }
        failure 
        {
            echo "Build failed!"
        }
    }
}
