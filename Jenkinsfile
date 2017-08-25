pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'start'
        echo 'DUDU'
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
            input(message: 'Ready to go?', submitterParameter: 'Proceed, Abort')
            
          },
          "long qa": {
            sleep 10
            
          }
        )
      }
    }
    stage('fail') {
      steps {
        sh 'date'
      }
    }
    stage('deploy') {
      steps {
        echo 'stop'
      }
    }
  }
  environment {
    DUDU = '23_DUDU'
    LOLO = '23_LOLO'
  }
}