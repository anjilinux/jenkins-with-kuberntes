pipeline {
agent any
stages{
  stage(" checkout from gitgub") {
    steps{
      checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/rritsoft/jenkins-with-kuberntes.git']])
      }

  }
      
    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "pod.yaml", kubeconfigId: "k8oldplugin")
        }
      }
    }  

  
   stage("another method step"){
     steps{
       script {
     sh 'kubectl apply -f  nginx1.yaml'
      }       
     }
   }
     
     
 }
}
