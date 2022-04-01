pipeline {
  agent any
  stages {
    stage('stg1') {
      parallel {
        stage('stg1') {
          steps {
            sh 'echo "this is stg1"'
            sleep 5
            echo 'wakeup'
          }
        }

        stage('stg2') {
          steps {
            echo ' i am stg2'
          }
        }

      }
    }

    stage('stg3') {
      steps {
        echo 'this is stg3'
      }
    }

    stage('stg4') {
      steps {
        build 'sdf'
        error 'byebye'
      }
    }

  }
}