pipeline{
    agent{
        label "node1"
    }
    tools{
        maven "maven3"

    }
    parameters {
  choice choices: ['production', 'development'], name: 'servers'
               }

    environment {
        userpasswd = "set%123"
    }
    stages{
        stage("build"){
            steps{
                echo "This is an build step $params.servers"
                sh "mvn clean package -DskipTests"
                }
        }
        stage("Test"){
            steps{
                echo "This is an Test step $userpasswd"
                }
        }
        stage("Deploy"){
            steps{
                echo "This is an deployment step"
                }
        }
    }
}