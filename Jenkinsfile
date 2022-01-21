pipeline {
  agent any
  stages {
    stage('checkout git') {
      steps {
        git(url: 'https://github.com/elestopadov/jenkins-example-app.git', branch: 'main')
      }
    }

    stage('Build') {
      steps {
        echo 'This is build'
      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy to DEV1') {
          steps {
            sleep 30
            echo 'Finished'
          }
        }

        stage('Deploy to Dev2') {
          steps {
            sleep 50
            echo 'completed'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'testing...'
      }
    }

  }
}