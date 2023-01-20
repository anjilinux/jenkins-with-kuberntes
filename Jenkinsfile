pipeline {
agent any
stages{
  stage(" checkout from gitgub"){
    steps{
      checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/rritsoft/jenkins-with-kuberntes.git']])
      }
  stage("run kube file") {
    steps{
        sh kubectl apply -f pod.yaml
    }
  } 
  
  }
    
  
}

}