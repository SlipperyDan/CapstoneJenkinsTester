pipeline {
  agent any
  stages {
    stage('Git Notification Received') {
      steps {
        git(url: 'https://github.com/SlipperyDan/CapstoneJenkinsTester', branch: 'CommitTest', credentialsId: 'c5ffccb3-a2a5-432e-8f6e-3216e66a9c67')
      }
    }

    stage('Kick Off A Powershell script') {
      steps {
        powershell 'Write-Host \'Jim is amazing\''
      }
    }

  }
}