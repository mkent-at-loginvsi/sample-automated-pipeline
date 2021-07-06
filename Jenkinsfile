pipeline {
  agent any
  stages {
    stage ('Stage 1 - Application Compatibility'){
      stage('Build') {
        steps {
          echo "Build Base OS"
          echo "Validate OS Build"
          echo "Install Applications"
          echo "Seal Image"
          echo "Publish Image"
        }
      }
      stage('Test') {
        steps {
          echo "Deploy Image"
          echo "Validate Image"
          echo "Test Applications"
          echo "Report Results"
        }
      }
      stage('Promote') {
        steps {
          echo "Promote Image"
        }
      }
    }
  }
}
