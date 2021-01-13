pipeline {
  tools{
    terraform 'terraform'
  }
  agent any
  stages{
    stage('Provisioning'){
      steps{
         sh label: '', script: 'terraform init'
         sh label: '', script: 'export PM_USER=th.giuseppe.zagaria; export PM_PASS=th.giuseppe.zagaria@!; terraform apply --auto-approve'
      }
    }
  }
}
