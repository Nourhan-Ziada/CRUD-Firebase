pipeline {
    agent any
    
    stages {

         stage('Set Execution Policy') {
            steps {
                // Set the execution policy for PowerShell scripts
                powershell 'Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass'
            }
        }
	stage('Clone PowerShell Script Repo') {
            steps {
                // Clone the repository containing the PowerShell script
                git url: 'https://github.com/Nourhan-Ziada/GoCartWorldE-CommerceSystem.git', branch: 'main'
            
                
            }
        }

        stage('List Directory Contents') {
            steps {
                // Execute the PowerShell script
                powershell './list_directory.ps1'
            }
        }
    }
}
