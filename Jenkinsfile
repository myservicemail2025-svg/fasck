pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git 'https://github.com/<твой_репозиторий>.git'
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
