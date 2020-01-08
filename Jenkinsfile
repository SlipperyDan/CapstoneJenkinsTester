pipeline {
  agent any
  stages {
    stage('Git Notification Received') {
      steps {
        git(url: 'https://github.com/SlipperyDan/CapstoneJenkinsTester', branch: 'CommitTest')
      }
    }

    stage('Kick Off A Powershell script') {
      steps {
        powershell 'Write-Host \'Jim is amazing\''
      }
    }

  }
}