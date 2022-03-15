pipeline
{
    agent any
    stages
    {
        stage('one')
        {
            steps
            {
                sh '''
                echo This is instruction one
                echo this is instruction two
                '''
            }
        }
        stage('two')
        {
            parallel
            {
                stage('two-one')
                {
                    steps
                    {
                        sh " echo This is stage two-one"
                    }
                }
                stage('two-two')
                {
                    steps
                    {
                        sh "echo This is stage two-two"
                    }
                }
            }
        }
    }
}