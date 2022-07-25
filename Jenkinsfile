pipeline {
    agent any
        stages {
           stage ("run frontend") {
              steps {
                echo "executing yarn"
                nodejs('Nodejs-10.17.0'){
                  sh 'yarn install'
                }
              }
           }
      
           stage ("run backend") {
               steps {
                   echo "executing gradel..."
                   withGradel() {
                       sh './gradelw -v'                       
                   }                    
               }

           }
}
