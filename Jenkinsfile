pipeline {
    agent any

    stages {
        stage('Build and Test Back End') {
            agent{docker{image "mcr.microsoft.com/dotnet/sdk:5.0"}}
            steps {
                sh "dotnet build"
                sh "dotnet test"
            }
            environment {
                DOTNET_CLI_HOME = "/tmp/DOTNET_CLI_HOME"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}