pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        echo 'Iniciando compilación'
      }
    }

    stage('Cambio de rama') {
      parallel {
        stage('Cambio de rama') {
          steps {
            sh 'git checkout answers4'
          }
        }

        stage('Texto') {
          steps {
            echo 'Cambiando de rama'
          }
        }

      }
    }

    stage('Maven install') {
      steps {
        sh 'mvn clean install'
        echo 'Compilaci�n completada'
      }
    }

  }
  environment {
    mensaje = ''
  }
}