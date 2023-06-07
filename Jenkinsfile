pipeline {
  agent any

  stages {
    stage('Clone repository') {
      steps {
        git branch: 'main', url: 'https://github.com/yash2880/node-app.git'
      }
    }

    stage('Build Docker image') {
      steps {
        sh 'sudo docker build -t node-app1:latest .'
      }
    }

    stage('Run Docker container') {
      steps {
        sh 'sudo docker run -p 80:3000 -d node-app1:latest'
      }
    }
  }
}
