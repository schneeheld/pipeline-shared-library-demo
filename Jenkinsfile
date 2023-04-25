@Library('pipeline-library-demo')_

pipeline {
    agent none
    stages {
        stage('Chapter-1') {
            agent any
            steps {
                withGroovy(tool:'4.0.11') {
                    printHeader 'Chapter 1'
                }
                echo 'Hello!'
            }
        }
        stage("Checkpoint.CH1") {
          agent none
          steps {
            checkpoint 'Completed checkpoint'
          }
        }
        stage('Chapter-2') {
            agent any
            steps {
                withGroovy(tool:'4.0.11') {
                    printHeader 'Chapter 2'
                 }
                echo 'Work is in progress....'
            }
        }
        stage("Checkpoint.CH2") {
          agent none
          steps {
              checkpoint 'Completed checkpoint'
          }
        }
        stage('Chapter-3') {
            agent any
            steps {
                withGroovy(tool:'4.0.11') {
                    printHeader 'Chapter 3'
                }
                echo 'Work is done.'
            }
        }
    }
}
