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
    stage('DESPLIEGUE') {
      steps {
        input(message: 'Quieres desplegar en pruebas?', id: 'desplieguePruebas', ok: 'ok')
      }
    }
  }
}