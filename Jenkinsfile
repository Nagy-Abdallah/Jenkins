pipeline {
  agent any
    environment {
        // DEOCKERHUB_CREDENTIALS = credentials('dockerhub')
      KUBECONFIG = credentials('minikube')
    }
  stages {
        stage('Deploy') {
            steps {
                script {
                    sh 'kubectl apply -f deployment.yaml'
                    sh 'kubectl apply -f service.yaml'
                }
            }
        }
    // stage  ("Install dependeincies") {
    //   agent {
    //     docker {image 'node:lts-buster-slim'}
    //   }
    //   steps {
    //     sh 'pwd'
    //     sh 'ls'
    //     sh 'npm install'
    //   }
    // }
    // stage ("Test"){
    //   agent {
    //     docker {image 'node:lts-buster-slim'}
    //   }      
    //   steps{
    //     sh 'npm run test'
    //   }
    // }

    // stage ("Build"){
    //   agent {
    //     docker {image 'node:lts-buster-slim'}
    //   }      
    //   steps{
    //     sh 'npm run build'
    //   }
    // }
    
  //   stage ("dockerBuild"){
  //   steps {
  //     sh 'docker build -t nagyadel/eclipse:${BUILD_NUMBER} .'
  //   }
  // }
  //   stage ("LoginANDPushImage"){
  //   steps {
  //   sh 'echo username = ${DEOCKERHUB_CREDENTIALS_USR}'
  //   sh 'echo passwrod = ${DEOCKERHUB_CREDENTIALS_PSW}'  
  //   sh 'docker login -u ${DEOCKERHUB_CREDENTIALS_USR} -p ${DEOCKERHUB_CREDENTIALS_PSW} '  
  //   sh 'docker push nagyadel/eclipse:${BUILD_NUMBER}' 
  //   }
  // }

  }
}
