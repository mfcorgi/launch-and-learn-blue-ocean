pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
      }
    }
    stage('Test') {
      steps {
        input 'Do you want to execute Tests?'
      }
    }
    stage('Unit Tests') {
      parallel {
        stage('Unit Tests') {
          steps {
            echo 'Unit Tests Executed'
          }
        }
        stage('Integration Tests') {
          steps {
            echo 'Integration Tests Executed'
          }
        }
        stage('Smoke Tests') {
          steps {
            echo 'Smoke Tests Executed'
          }
        }
        stage('Performance Tests') {
          steps {
            echo 'Performance Tests Executed'
          }
        }
      }
    }
    stage('Confirmation') {
      steps {
        input 'Do you want to deploy?'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy Done!'
      }
    }
  }
}