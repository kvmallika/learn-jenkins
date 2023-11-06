pipeline {

  agent {
    node {
      label 'workstation'
    }
  }

  options {
    ansiColor('xterm')
  }
  parameters {
          string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

    }
  environment {
    SAMPLE_URL = "test.com"
  }


    stages {
        stage('one') {
          steps {
            sh 'echo Hello World'
            sh 'echo ${SAMPLE_URL}'
          }
        }
    }
    post {
      always {
        sh 'echo Post CleanUP steps '

      }
    }

}