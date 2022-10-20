pipeline {
  agent any
  stages {
    stage('Build') {
      agent any
      steps {
        sh ' ./gradlew build '
      }
    }

    stage('Test') {
      steps {
        sh './gradlew check'
      }
    }

  }
  post {
          always {
              archiveAritifacts artifacts: 'build/libs/**/*.jar',fingerprint:true
              junit 'build/reports/**/*.xml'
          }
      }
}