pipeline {
  options {
    disableConcurrentBuilds()
  }
  agent {
    label "jenkins-jx-base"
  }
  environment {
    DEPLOY_NAMESPACE = "jx-staging"
  }
  stages {
    stage('Validate Environment') {
      steps {
        container('jx-base') {
          dir('pkshelm') {

               sh 'jx step helm apply --name pkshelm'
       //  sleep 120
           sh 'jx step helm install --name=pkshelm pkshelm'
        //       sh 'jx step helm apply'
        
       
       }
        }

      }
    }
  }
}
