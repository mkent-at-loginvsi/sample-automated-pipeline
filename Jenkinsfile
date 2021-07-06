pipeline {
  agent any

  stages {
    stage('Application Compatibility') {
      stages {
        stage ('Build OS') {
          steps {
            echo "1.1"
          }
        }
        stage ('Install Apps') {
          steps {
            echo "1.2"
          }
        }
      }
    }

    stage('Performance Testing') {
      stages {
        stage('Build OS') {
          steps {
            echo "2.1"
          }
        }
      }
    }
  }
}
