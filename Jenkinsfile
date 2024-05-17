pipeline {
  agent { label 'linuxslave1'}
  stages {
    stage('Stage 1') {
      steps {
        echo 'Hello world!'
      }
    }

    stage('checkout') {
      steps {
        git(url: 'https://github.com/Vinaysh259/demoJenkinsfile.git', branch: 'master')
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
