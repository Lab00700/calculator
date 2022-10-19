pipeline {
  agent any
  stages {
    stage('Compile') {
      agent any
      steps {
        sh ' ./gradlew clean '
      }
    }

    stage('Test') {
      steps {
        sh './gradlew test'
      }
    }

  }
}