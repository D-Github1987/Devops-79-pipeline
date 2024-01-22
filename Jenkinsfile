pipeline {
  agent any
  stages {
    stage('Dev') {
      steps {
        echo 'Development'
      }
    }

    stage('Build') {
      steps {
        echo 'Building Stage'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
      }
    }

    stage('UAT') {
      parallel {
        stage('UAT') {
          steps {
            echo 'Quality Check'
          }
        }

        stage('Deploy') {
          steps {
            echo 'Deoloy'
          }
        }

        stage('Final') {
          steps {
            echo 'Final Check'
          }
        }

      }
    }

    stage('Prod') {
      steps {
        echo 'Production'
      }
    }

  }
}