pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        echo 'Iniciando compilaciÃ³n'
      }
    }

    stage('Cambio de rama') {
      parallel {
        stage('Cambio de rama') {
          steps {
            sh 'git branch --all'
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
        echo 'Compilación completada'
      }
    }

  }
  environment {
    mensaje = ''
  }
}