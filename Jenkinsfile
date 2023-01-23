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
          kubernetesDeploy(configs: "pod.yaml,
                                     nginx1.yaml"
                           kubeconfigId: "k8oldplugin")
          
          
        }
      }
    }  

  
     
 }
}
