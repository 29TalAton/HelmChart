pipeline{
        agent any
         stages{
              
              stage("Deploy to Dev") {
                   steps {
                            sh "helm install simple-web-app devops-tal/ --values devops-tal/values.yaml --namespace tal"
                              
                          }
                         }
       }
     }
