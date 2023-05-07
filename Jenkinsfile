pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''pwd
date
echo "hello world"'''
      }
    }

    stage('Test') {
      parallel {
        stage('parallel Test1') {
          steps {
            echo 'test message'
            sh 'date'
          }
        }

        stage('parallel Test2') {
          steps {
            sleep 2
            echo 'parallel'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'End**'
      }
    }

  }
}