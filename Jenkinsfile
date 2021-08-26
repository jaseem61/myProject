pipeline {
  agent { label 'master' }
  tools {
    maven 'apache-maven-3.8.1'
  }
  stages {
    stage('checkout') {
      steps {
        git 'https://github.com/jaseeeeeeeem/myProject.git'
      }
    }
    stage('Build') {
      steps {
        bat 'mvn clean compile'
      }
    }
    stage('Test') {
      steps {
        bat 'mvn test'
        junit '**/target/surefire-reports/TEST-*.xml'
      }
    }
    stage('Package') {
      steps {
        bat 'mvn package'
      }
    }
  }
}
