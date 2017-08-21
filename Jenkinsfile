pipeline {
  agent any
  stages {
    stage('buil') {
      steps {
        svn(url: 'http://192.168.33.11/svn/testrepo/', poll: true, changelog: true)
      }
    }
    stage('') {
      steps {
        parallel(
          "t1": {
            sh 'lsb_release -a'
            
          },
          "t2": {
            node(label: 'node1') {
              sh 'ls'
              sh 'date'
            }
            
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
            build 'a job in pipeline'
            
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