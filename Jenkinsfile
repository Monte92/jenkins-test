pipeline {
    agent any

    stages {
		stage('Restore') {
			steps { sh 'cd JenkinsTest && dotnet restore JenkinsTest.sln' }
		}

		stage('Build') {
			steps { sh 'cd JenkinsTest && dotnet build JenkinsTest.sln --configuration Release' }
		}

		stage('Run') {
			steps { sh 'cd JenkinsTest && dotnet run --project JenkinsTest.csproj' }
		}
    }
}
