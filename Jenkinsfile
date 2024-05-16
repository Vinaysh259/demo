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
        git(url: 'https://github.com/Vinaysh259/demoJenkinsfile.git', branch: 'master', poll: true)
      }
    }

    stage('build') {
      steps {
        sh 'python3 hello.py'
      }
    }

  }
}