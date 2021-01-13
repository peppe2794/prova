pipeline {
  tools{
    terraform 'terraform'
  }
  agent any
  stages{
    stage('Provisioning'){
      steps{
        withCredentials([usernamePassword(credentialsId: 'Proxmox', passwordVariable: 'PASSWORD', usernameVariable: 'USER')]) {
          sh label: '', script: 'terraform init'
          sh label: '', script: 'export PM_USER=${USER}; export PM_PASS=${PASSWORD}; terraform apply --auto-approve'
        }
      }
    }
  }
}
