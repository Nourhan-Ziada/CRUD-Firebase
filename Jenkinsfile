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
                // Ensure the PowerShell script path is correct and execute it
                script {
                    def psScriptPath = "${pwd()}/list_directory.ps1"
                    echo "Executing script at: ${psScriptPath}"
                    
                    // Execute the PowerShell script
                    powershell """
                        cd ${pwd()}
                        ./list_directory.ps1
                    """
                }
            }
        }
    }
}
