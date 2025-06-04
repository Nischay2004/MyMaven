pipeline {
  agent any
  tools {
    maven 'Maven'
    jdk 'JDK'
  }
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/Nischay2004/MyMaven.git'
      }
    }
    stage('Build') {
      steps {
        sh 'mvn clean install'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }
    stage('Run Application') {
      steps {
        sh 'mvn exec:java -Dexec.mainClass=com.example.App'
      }
    }
  }
}
