pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build competed'
        retry(count: 3) {
          echo 'Trying to Build'
        }

      }
    }

    stage('Test1') {
      parallel {
        stage('Test1') {
          steps {
            echo 'Running test1'
          }
        }

        stage('Test 2') {
          steps {
            echo 'Running Test2'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are you Sure to Deploy', ok: 'Yes , i\'m Sure')
        echo 'Deployment Done'
      }
    }

  }
}