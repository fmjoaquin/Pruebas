pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building..'
        git 'https://github.com/kliakos/sparkjava-war-example.git'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing..'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
  }
}