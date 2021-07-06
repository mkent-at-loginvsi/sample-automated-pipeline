pipeline {
  agent any

  stages {
    stage('Application Compatibility') {
      stages {
        stage ('Build base OS') {
          steps {
            echo "Provision Instance (Azure Plugin)"
            echo "Build Image (Login AM Plugin)"
          }
        }
        stage ('Install Applications') {
          steps {
            echo 'Install Packages (Login AM Plugin) = Apps'
          }
        }
        stage ('Performance Optimizations') {
          steps {
            echo 'Install Packages (Login AM Plugin) = Reg Configs'
          }
        }
        stage ('Create Image Artifact') {
          steps {
            echo 'Seal Image'
            echo 'Publish Image Artifact'
          }
        }

      stage ('Acceptance Test') {
        steps {
          echo 'Deploy Image from published template'
          echo 'Run Application Group Acceptance Test = Apps (Login Enterprisese Plugin - Desktop Connector?)'
        }
      }

    }
  }

    stage('Application and Infrastructure Load (Performance Testing)') {
      stages {
        stage ('Scale up') {
          steps {
            echo 'Deploy Image from published template (Login AM Plugin - Collection?)'
          }
        }
        stage ('Load Test') {
          steps {
            echo 'Run Application Group Load Test = Apps (Login Enterprisese Plugin - Desktop Connector?)'
          }
        }
      }
    }

    stage('Performance and Availablity (Continuous Test)') {
      stages {
        stage ('Rollout') {
          steps {
            echo 'Deploy Image from published template (Login AM Plugin - Collection?)'
          }
        }
        stage ('Continuous Test') {
          steps {
            echo 'Run Application Group Continuous Test = Apps (Login Enterprisese Plugin - Desktop Connector?)'
          }
        }
      }
    }
  }
}
