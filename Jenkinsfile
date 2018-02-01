pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Bajando Codigo'
        git 'https://github.com/kliakos/sparkjava-war-example.git'
        echo 'COnstruyendo'
        bat 'mvn -Dmaven.test.failure.ignore=true install' 
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
