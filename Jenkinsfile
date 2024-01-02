pipeline {
  agent any
  stages {
    stage('verify version') {
      steps {
        //sh 'php --version'
        println('Hello worlds');
      }
    }
    stage('Composer Install') {
        sh 'composer install'
    }
    stage("PHPLint") {
        sh 'find app -name "*.php" -print0 | xargs -0 -n1 php -l'
    }
    stage("PHPUnit") {
        sh 'vendor/phpunit/phpunit/phpunit --bootstrap build/bootstrap.php --configuration phpunit-coverage.xml'
    }    
    stage('hello') {
      steps {
        sh 'hello.php'
      }
    }
  }
}
