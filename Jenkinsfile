pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm 
            }
        }
        stage('Restore the project') {
            steps {
                bat 'dotnet restore Horizons.sln'
            }
        }

        stage('Build the project up') {
            steps {
                bat 'dotnet build Horizons.sln'
            }
        }

        stage('Test the project') {
            steps {
                bat 'dotnet test Horizons.sln --no-build --verbosity normal'
            }
        }
    }
}