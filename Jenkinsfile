pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        https://github.com/myservicemail2025-svg/fasck.git
      }
    }
    stage('Build Docker Image') {
      steps {
        sh 'docker build -t flask-app .'
      }
    }
    stage('Deploy') {
      steps {
        sh 'docker compose down || true'
        sh 'docker compose up -d'
      }
    }
  }
}
