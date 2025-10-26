pipeline {
    agent any

    stages {
        stage("Restore the dependencies") {
            steps {
                bat 'dotnet restore'
            }
        }
        
        stage("Build the application") {
            steps {
                bat 'dotnet build --no-restore'
            }
        }
        
        stage("Run the Tests") {
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}