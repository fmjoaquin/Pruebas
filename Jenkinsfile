pipeline {
  agent any
  stages {
    stage('COMPILADO') {
      steps {
        echo 'Hola mundo pipelines'
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