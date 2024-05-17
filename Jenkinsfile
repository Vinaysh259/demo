pipeline {
  agent any
  stages {
    stage('Stage 1') {
      steps {
        echo 'Hello world!'
      }
    }

    stage('checkout') {
      steps {
        git branch: 'master',
            credentialsId: 'github_ssh'
            url: 'git@github.com:Vinaysh259/demoJenkinsfile.git'

            sh "ls -lat"
      }
    }


    stage('build') {
      steps {
        sh 'python3 hello.py'
      }
    }

    stage('docker build') {
      steps {
        sh 'docker build -t demo:latest .'
      }
    }

  }
}
