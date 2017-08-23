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
            svn(url: 'http://192.168.33.11/svn/testrepo/', changelog: true, poll: true)
            
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
}