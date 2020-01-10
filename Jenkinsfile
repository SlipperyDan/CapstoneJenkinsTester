pipeline {
  agent any
  stages {
    stage('Git Notification Received') {
      steps {
        git(url: 'https://github.com/SlipperyDan/CapstoneJenkinsTester', branch: 'CommitTest', credentialsId: 'c5ffccb3-a2a5-432e-8f6e-3216e66a9c67', changelog: true)
      }
    }

    stage('Kick Off A Powershell Script') {
      parallel {
        stage('Kick Off A Powershell Script') {
          steps {
            powershell 'Write-Host \'I wildly misunderstood how this pipeline tool works\''
          }
        }

        stage('Start linux via Powershell') {
          steps {
            powershell 'C:\\Users\\Daniel\\Desktop\\ThisWasMadeViaDebian\\tester.sh'
          }
        }

      }
    }

  }
}