pipeline {
    agent any
    
    stages {

	stage('Clone PowerShell Script Repo') {
            steps {
                // Clone the repository containing the PowerShell script
                git url: 'https://github.com/Nourhan-Ziada/GoCartWorldE-CommerceSystem.git', branch: 'main'
            
                
            }
        }

        stage('List Directory Contents') {
            steps {
                // Execute the PowerShell script
                bat ' call GoCartWorldE-CommerceSystem\\list_files.bat'
            }
        }
    }
}
