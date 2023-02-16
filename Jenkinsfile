pipeline
{
    agent any
    stages
    {
        stage ('Build')
        {
            steps
            {
                sh 'g++ pes1ug20cs087_task5.cpp -o pes1ug20cs087_task5'
                echo 'build stage successful'
                build job: 'PES1UG20CS087-1'
            }
        }
        stage ('Test')
        {
            steps
            {
                sh './pes1ug20cs087_task5'
                echo 'test stage successful'
            }
        }
        stage ('Deploy')
        {
            steps
            {
                echo 'deployment successful'
            }
        }
    }
    post
    {
        failure
        {
            echo 'pipeline failed'
        }
    }
}
