pipeline {
    agent any
    stages {
            stage('Compile Stage') {
                steps {
                    withMaven(maven : 'Maven-3.6.1')
                    'mvn clean compile'
                }
            }

         stage('Build Stage') {
               steps {
                   withMaven(maven : 'Maven-3.6.1')
                   'mvn install'
                  }
         }

        stage('Testing Stage') {
              steps {
                  withMaven(maven : 'Maven-3.6.1')
                  'mvn test'
                 }
           }
        stage('Deploy Stage') {
            agent {
            echo 'Deploying...'
            }
        }
    }
}
