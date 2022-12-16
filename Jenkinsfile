pipeline {
  agent any
  stages {
    stage('buid') {
      steps {
        sh 'echo "$(date)"'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'hellow test'
            echo 'test complete'
          }
        }

        stage('test2') {
          steps {
            echo 'all done'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        input(message: 'are you sure to deploy ', ok: 'yes')
      }
    }

    stage('Notify') {
      steps {
        echo 'new build success '
      }
    }

  }
}