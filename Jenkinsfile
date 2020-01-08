pipeline {
  agent any
  stages {
    stage('Git Notification Received') {
      steps {
        git(url: 'https://github.com/SlipperyDan/CapstoneJenkinsTester', branch: 'CommitTest')
      }
    }

    stage('Kick Off A Powershell script') {
      parallel {
        stage('Kick Off A Powershell script') {
          steps {
            powershell 'Write-Host \'Jim is amazing\''
          }
        }

        stage('Kick off a bash script') {
          steps {
            sh '''#! /bin/bash

clear

echo "There has to be something going on with Dockr for this to be working. "'''
          }
        }

      }
    }

  }
}