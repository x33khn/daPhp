pipeline {
  agent any
  stages {
    stage('verify version') {
      steps {
        sh '/usr/bin/php --version'
      }
    }
    stage('hello') {
      steps {
        sh '/usr/bin/php hello.php'
      }
    }
  }
}
