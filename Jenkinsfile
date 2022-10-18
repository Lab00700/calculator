pipeline {
  agent any
  stages {
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            sh './gradlew check'
          }
        }

        stage('Compile') {
          steps {
            sh ' gradlew(\'clean\', \'classes\')'
          }
        }

      }
    }

  }
}