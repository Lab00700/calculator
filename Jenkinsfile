pipeline {
  agent any
  stages {
    stage('Compile') {
      agent any
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