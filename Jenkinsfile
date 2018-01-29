pipeline {
  agent any
  stages {
    stage('COMPILADO') {
      steps {
        svn 'https://svn.justicia.es/OTROS/FRAMEWORK20/TRUNK/Codigo/PB3'
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