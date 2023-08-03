pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Powershell Script Generator') {
            steps {
                 powershell 'Write-Output "Hello PowerShell!"'
            }
        }
        stage('Jenkin Environment Varibale'){
            steps{
            echo "$GIT_BRANCH"
            }
        }
        stage('Docker Build') {
         steps {
            pwsh(script: 'docker images -a') // PWSH --> Since its run on Windows so we are using Powershell Core
            pwsh(script: """
               cd azure-vote/
               docker images -a
               docker build -t jenkins-pipeline .
               docker images -a
               cd ..
            """)
         }
      }
    }
}
