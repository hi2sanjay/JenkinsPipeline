pipeline {
    agent any
    stages {
            stage('Compile Stage') {
                steps {
                    withMaven(maven : 'Maven-3.6.1')
                    run 'mvn clean compile'
                }
            }

         stage('Build Stage') {
               steps {
                   withMaven(maven : 'Maven-3.6.1')
                   run 'mvn clean install'
                  }
         }

        stage('Testing Stage') {
              steps {
                  withMaven(maven : 'Maven-3.6.1')
                  run 'mvn clean test'
                 }
           }
        stage('Deploy Stage') {
            agent {
            echo 'Deploying...'
            }
        }
    }
}
