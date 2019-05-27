pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        git(url: 'https://github.com/NickHub4017/JenkTest/', branch: 'develop')
      }
    }
    stage('run') {
      steps {
        sh '''ls
pwd
yarn start'''
      }
    }
  }
}