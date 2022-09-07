pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/elestopadov/jenkins-example-app.git', branch: 'main')
      }
    }

    stage('Build') {
      steps {
        echo 'Is Build'
      }
    }

    stage('Deploy') {
      parallel {
        stage('DeployToDev1') {
          steps {
            sleep 30
            echo 'Finished'
          }
        }

        stage('DeployToDev2') {
          steps {
            sleep 30
            echo 'Completed'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'Test finished'
      }
    }

  }
}