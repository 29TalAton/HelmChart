pipeline{
    agent any
    parameters {
        string(name: "Name", defaultValue: "simple-web-app", description: "please enter deployment name")
        choice(name: 'Action', choices: 'Deploy\nDestroy\n', description: "")
    }   
    stages{
        stage("Deploy to Dev") {
            when {
        expression {
            params.Action == 'Deploy'
        }
    }
            steps {
                 sh "helm install simple-web-app devops-tal/ --values devops-tal/values.yaml --namespace tal"
                 }
        }
    }
}
