pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Goodbye') {
            steps {
                echo 'Goodbye World'
            }
        }
        stage('Powershell Script Generator') {
            steps {
                 powershell 'Write-Output "Hello PowerShell!"'
            }
        }
    }
}
