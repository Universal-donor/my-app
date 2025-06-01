pipeline
 { agent any
   environment {
     IMAGE = "ghcr.io/my-org/sample-node-app:${env.BRANCH_NAME}
   }
  stages{
    stage('Clone'){
      steps{
      git url: 'https://github.com/Universal-donor/my-app'
    }}
    stage('Build docker image'){
      steps{
        script {
          sh "docker build -t $IMAGE ."
        }
      }
    }
    stage('Deploy') {
      steps {
        sh "echo Deploying $IMAGE to K8s/OpenShift (mock step)"
      }
    }
  }
}
