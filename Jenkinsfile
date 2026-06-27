pipeline {
    agent any

    stages {
        stage('Check .NET') {
            steps {
                bat 'dotnet --version'
            }
        }

        stage('Restore') {
            steps {
                bat 'dotnet restore Homies.sln'
            }
        }

        stage('Build') {
            steps {
                bat 'dotnet build Homies.sln --configuration Release --no-restore'
            }
        }

        stage('Test') {
            steps {
                bat 'dotnet test Homies.sln --configuration Release --no-build --verbosity normal'
            }
        }
    }
}