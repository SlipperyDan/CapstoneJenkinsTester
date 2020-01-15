pipeline {
  agent any
  stages {
    stage('Git Notification Received') {
      steps {
        git(url: 'https://github.com/SlipperyDan/CapstoneJenkinsTester', branch: 'CommitTest', credentialsId: 'c5ffccb3-a2a5-432e-8f6e-3216e66a9c67', changelog: true)
      }
    }

    stage('Build Ec2 Instance') {
      steps {
        powershell 'C:\\Users\\Daniel\\Desktop\\ThisWasMadeViaDebian\\zoop.ps1'
      }
    }

    stage('Unit Test') {
      steps {
        echo 'Pushed to week 3'
      }
    }

    stage('Return Results') {
      steps {
        echo 'Week 4'
      }
    }

    stage('Update Prod.') {
      steps {
        powershell 'C:\\Users\\Daniel\\Desktop\\ThisWasMadeViaDebian\\CopyWebsiteUpdateS3Bucket.ps1'
      }
    }

  }
}