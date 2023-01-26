pipeline {
agent any
stages{
  stage("checkout from git "){
    steps {
        checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/rritsoft/jenkins-with-kuberntes.git']])
    }
  }       
 stage("docker build image") {
    steps{
        sh 'docker build -t  anjireddy3993/nginx:latest . '
        sh 'docker images'
        sh 'docker login -u anjireddy3993  -p ASDasd123$'
        sh 'docker push  anjireddy3993/nginx:latest'
        echo " all is success"

    }
 }



    }
}
