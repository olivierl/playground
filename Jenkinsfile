pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'npm install'
        echo 'npm run build'
      }
    }
    stage('test') {
      parallel {
        stage('unit tests') {
          agent any
          steps {
            echo 'Unit tests'
          }
        }
        stage('integration tests') {
          steps {
            echo 'Integration tests'
          }
        }
        stage('functional tests') {
          steps {
            echo 'Functional tests'
          }
        }
      }
    }
    stage('release') {
      steps {
        echo 'release'
      }
    }
    stage('deploy') {
      steps {
        echo 'deploy'
      }
    }
  }
}