pipeline {
  tools{
    terraform 'terraform'
  }
  agent any
  stages{
    stage('Provisioning'){
      steps{
         sh label: '', script: 'terraform init'
         sh label: '', sript: 'terraform apply --auto-approve'
      }
    }
  }
}
