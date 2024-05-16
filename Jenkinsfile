pipeline {
    agent any
    
    stages {
         stage('Set Execution Policy') {
            steps {
                // Set the execution policy for PowerShell scripts
                powershell 'Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass'
            }
        }
        stage('List Directory Contents') {
            steps {
                // Execute the PowerShell script
                powershell './list_directory.ps1"'
            }
        }
    }
}