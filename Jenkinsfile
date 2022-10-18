pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh ' gradlew(\'clean\', \'classes\')'
      }
    }

    stage('Test') {
      steps {
        sh './gradlew check'
      }
    }

  }
}