pipeline {
   agent any

   tools {nodejs "Node16"}

   environment {
       CHROME_BIN = '/bin/google-chrome'
      
   }

   stages {
       stage('Dependencies') {
           steps {
               sh 'npm install -g'
           }
       }
       stage('Dependencies') {
           steps {
               sh 'npm install -g cypress'
           }
       }
       stage('e2e Tests') {
                  steps {
                sh 'npm cypress run'
                  }
              }
       stage('Deploy') {
           steps {
               echo 'Deploying....'
           }
       }
   }
}
