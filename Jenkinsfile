pipeline {
   agent any

   tools {nodejs "Node"}

   environment {
       CHROME_BIN = '/bin/google-chrome'
      
   }

   stages {
       stage('Dependencies') {
           steps {
               bat 'npm i'
               bat 'npm install cypress --save-dev'
           }
       }
       stage('Build application')
       {
        steps {
            bat 'npm run dev &'
        }
       }
       stage('Run Tests') {
                  steps {
                bat 'npm run cy:run'
                  }
               }
    }
}