pipeline {
  agent any
  stages {
    stage('prepare_job') {
      steps {
        sleep 15
      }
    }

    stage('build_job') {
      steps {
        echo 'Start build job'
      }
    }

    stage('run_job') {
      parallel {
        stage('run_nfvo_job') {
          steps {
            sleep 20
            sleep 12
          }
        }

        stage('run_vnfm_job') {
          steps {
            sleep 15
            sleep 12
          }
        }

        stage('run_vsd_job') {
          steps {
            sleep 15
          }
        }

      }
    }

    stage('get_result') {
      steps {
        sleep 1
      }
    }

    stage('finished') {
      steps {
        echo 'run finished'
      }
    }

  }
}