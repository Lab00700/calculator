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
    stage('Run') {
          agent any
          steps {
            sh 'java -jar gradle/wrapper/*.jar'
          }
        }
  }

}