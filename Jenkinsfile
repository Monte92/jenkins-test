pipeline {
    agent any

    stages {
		stage('Restore') {
			steps { sh 'dotnet restore JenkinsTest.sln' }
		}

		stage('Build') {
			steps { sh 'dotnet build JenkinsTest.sln --configuration Release' }
		}

		stage('Run') {
			steps { sh 'dotnet run --project JenkinsTest.csproj' }
		}
    }
}
