pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building code'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'echo "Started testing"'
          }
        }

        stage('IT') {
          steps {
            sh 'echo "Running ITs"'
          }
        }

        stage('UAT') {
          steps {
            sh 'echo "User Accepance tests"'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        sh 'echo "deploypackage"'
      }
    }

  }
}