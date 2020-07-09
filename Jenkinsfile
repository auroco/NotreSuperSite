pipeline {
   agent any
   
   environment {
        def URL_PROJECT = "https://github.com/auroco/NotreSuperSite.git"
   }

   stages {
      stage('Lancement du build AMI') {
          steps {
            build job: 'Build-AMI', parameters: [[$class: 'StringParameterValue', name: 'URL_PROJECT', value: URL_PROJECT]]
          }
      }
   }
}
