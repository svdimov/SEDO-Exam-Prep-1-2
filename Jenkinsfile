pipeline{
    agent any{
        
    }
    stages{
        stage("Restore dependencies"){
            when{anyOf{
                branch "master"
                branch "develop"
            }}
            steps{
                bat "dotnet restore"
            }
            

        }
        stage("Build"){
            when{anyOf{
                branch "master"
                branch "develop"
            }}
            steps{
                bat "dotnet build --no-restore"
            }
            

        }
              stage("Run tests"){
            when{anyOf{
                branch "master"
                branch "develop"
            }}
            steps{
                bat "dotnet test --no-build --verbosity normal"
            }
            

        }
    }
 
}