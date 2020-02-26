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

    stage('Delete Deprecated Local Repository') {
      steps {
        powershell 'C:\\Users\\Daniel\\Desktop\\ThisWasMadeViaDebian\\DeleteCapstoneJenkinsTester.ps1'
      }
    }

    stage('Download New Repository') {
      steps {
        powershell 'C:\\Users\\Daniel\\Desktop\\ThisWasMadeViaDebian\\CloneGithubRepositoryUpdateWebsite.ps1'
      }
    }

    stage('Download the Results') {
      steps {
        powershell 'C:\\Users\\Daniel\\Desktop\\ThisWasMadeViaDebian\\downloadtheresults.ps1'
      }
    }

    stage('Check if Failed ') {
      steps {
        warnError(message: 'See Documentation For Results') {
          powershell 'C:\\Users\\Daniel\\Desktop\\ThisWasMadeViaDebian\\CheckIfFail'
        }

      }
    }

    stage('DAB') {
      steps {
        echo ':\'('
      }
    }

    stage('FORTHELOVEOFGOD') {
      steps {
        echo ':")'
      }
    }

  }
}