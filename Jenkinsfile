pipeline {
  agent any
  stages {
    stage('Compile') {
      agent any
      steps {
        sh ' ./ gradlew clean '
      }
    }

    stage('Test') {
      steps {
        sh './gradlew check'
      }
    }

    stage('Build') {
      steps {
        sh './gradlew build'
      }
    }

  }
}