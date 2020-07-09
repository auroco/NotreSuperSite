pipeline {
   agent any
   
   environment {
        def URL_PROJECT = "https://github.com/auroco/NotreSuperSite.git"
        def ACTION = "Full Build"
   }

   stages {
      stage('Lancement du build AMI') {
          steps {
            build job: 'Build-AMI', parameters: [[$class: 'StringParameterValue', name: 'URL_PROJECT', value: URL_PROJECT]]
          }
      }
      
      stage('Construction infra') {
          steps {
            build job: 'DeployInfra', parameters: [[$class: 'StringParameterValue', name: 'action', value: ACTION]]
          }
      }
   }
}
