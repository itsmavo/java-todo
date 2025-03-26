pipeline{
    agent any
    tools{
        gradle "gradle"
    }
    stages{
        stage("Cloning repository"){
            steps{
                git branch:"master", url:"https://github.com/itsmavo/java-todo.git"
            }
        }
        stage("Build Code"){
            steps{
                sh "gradle build"
            }
        }
        stage("Testing Code"){
            steps{
                sh "gradle test"
            }
        }
    }
}