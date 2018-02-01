pipeline {
  agent any
  tools {
        maven 'Maven 3.3.9'
        jdk 'jdk8'
    }
  stages {
    stage('COMPILADO') {
      steps {
        echo 'Hola mundo pipelines'
        git 'https://github.com/kliakos/sparkjava-war-example.git'
      }
    }
	stage ('Build') {
		steps {
			sh 'mvn -Dmaven.test.failure.ignore=true install' 
		}		
    }
    stage('TEST') {
      steps {
        echo 'Hola'
      }
    }
    stage('DESP. DESA') {
      steps {
        input(message: 'Quieres desplegar en pruebas?', id: 'desplieguePruebas', ok: 'ok')
      }
    }
    stage('DESP. PRU') {
      steps {
        echo 'He desplegado en pruebas'
      }
    }
    stage('DESP. PRE') {
      steps {
        echo 'He desplegado en pre'
      }
    }
    stage('DESP. PRO') {
      steps {
        echo 'He desplegado en pro'
      }
    }
  }
}
