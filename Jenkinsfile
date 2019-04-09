pipeline {
  agent {
    node {
      label '.Net-FCCT-02'
    }

  }
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/narendrasingamaneni91/FCCT_ACTS_UFT_TEST.git', branch: 'master', credentialsId: 'unis88')
      }
    }
    stage('build') {
      steps {
        bat 'CScript %WORKSPACE%\\TestRunner.vbs'
      }
    }
  }
}