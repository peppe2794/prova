pipeline {
  tools{
    terraform 'terraform'
  }
  agent any
  stages{
    stage('Provisioning'){
      steps{
         sh label: '', script: 'export PM_USER=th.giuseppe.zagaria'
         sh label: '', script: 'terraform init'
         sh label: '', script: 'terraform apply --auto-approve'
      }
    }
  }
}
