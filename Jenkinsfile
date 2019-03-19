pipeline {
     agent any
         stages {
             stage('First') {
                 steps {
                      script {
                          env.EXECUTE="True"
                      }
                 }
             }
               stage('Second') {
                   when {
                      environment name: 'EXECUTE', value: "True"
                    }
                 steps {
                     sh ' echo "Updating Second Stage" '
                 }
             }
              stage('Third') {
                   when {
                      environment name: 'EXECUTE', value: "True"
                   }
                 steps {
                     sh ' echo "Updating Third Stage" '
                 }
             }
         }
 }
