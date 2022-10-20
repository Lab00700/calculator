pipeline {
  agent any
  stages {
    stage('Compile') {
      agent any
      steps {
        sh ' ./gradlew compileJava'
      }
    }

    stage('Test') {
      steps {
        sh './gradlew check'
      }
    }
stage('Build') {
      agent any
      steps {
        sh ' ./gradlew build '
      }
    }
    }
    post {
        always{
            archiveArtifacts artifacts: 'build/libs/*.jar', fingerprint:true
            junit 'build/reports/**/*.xml'

        }

    }

}