pipeline
{
    agent any
    environment 
    {
        MAVEN_GOALS = 'clean install'        // Define the Maven goals for building the project  
    }
    stages
    {
        stage('Checkout') 
        {
            steps
            {
                // Checkout the Git repository
                git credentialsId: 'f0a39c8f-060d-4e48-a81d-e7e37e8c7254', url: 'https://github.com/Bheeshma0308/build1.git'
                // checkout([$class:'GitSCM',branches:[[name: '*/master']],doGenerateSubmoduleConfigurations:false,userRemoteConfigs:[[url:'https://github.com/Bheeshma0308/build1.git']]])
            }
        }
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
