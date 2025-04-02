pipeline{
    agent{
        label "node1"
    }
    parameters {
        string defaultValue: 'production', name: 'server'
    }

    stages{
        stage("build"){
            steps{
                echo "This is an build step $params.server"
                }
        }
        stage("Test"){
            steps{
                echo "This is an Test step"
                }
        }
        stage("Deploy"){
            steps{
                echo "This is an deployment step"
                }
        }
    }
}