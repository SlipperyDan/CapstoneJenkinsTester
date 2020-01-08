pipeline {
  agent any
  stages {
    stage('Git Notification Received') {
      steps {
        git(url: 'https://github.com/SlipperyDan/CapstoneJenkinsTester', branch: 'CommitTest')
      }
    }

    stage('Kick Off A Powershell Script') {
      steps {
        powershell 'Write-Host \'I wildly misunderstood how this pipeline tool works\''
      }
    }

  }
}