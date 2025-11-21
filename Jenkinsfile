pipeline {
    agent {
        docker {
            image 'mcr.microsoft.com/dotnet/sdk:9.0'
            args '-u root'   // optional: prevents file-permission issues
        }
    }

    stages {

        stage('Restore') {
            steps {
                sh 'dotnet restore JenkinsTest.sln'
            }
        }

        stage('Build') {
            steps {
                sh 'dotnet build JenkinsTest.sln --configuration Release'
            }
        }

        stage('Run') {
            steps {
                sh 'dotnet run --project JenkinsTest.csproj'
            }
        }
    }
}
