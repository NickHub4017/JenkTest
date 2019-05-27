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
        sh '''curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -y
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

apt-get update && apt-get install yarn
'''
      }
    }
  }
}