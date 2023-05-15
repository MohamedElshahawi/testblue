pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build competed'
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

    stage('Depoy') {
      steps {
        echo 'Deployment Done'
      }
    }

  }
}