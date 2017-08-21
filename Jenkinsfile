pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'start'
      }
    }
    stage('test') {
      steps {
        parallel(
          "t1": {
            sh 'lsb_release -a'
            
          },
          "t2": {
            sh 'date'
            
          }
        )
      }
    }
    stage('qa') {
      steps {
        parallel(
          "qa": {
            echo 'dfdfsdfs'
            
          },
          "qa2": {
            echo 'qa2 log'
            
          },
          "long qa": {
            sleep 10
            
          }
        )
      }
    }
    stage('fail') {
      steps {
        sh 'sdsdasdadad'
      }
    }
    stage('deploy') {
      steps {
        echo 'stop'
      }
    }
  }
}