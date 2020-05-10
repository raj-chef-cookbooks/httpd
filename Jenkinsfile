pipeline {
  agent any
  stages {
    stage('Patch OS') {
      steps {
        sh 'echo "sudo yum update -y" '
      }
    }
    stage('Install Essential rpms') {
      steps {
        script {
          def wgetExists = fileExists '/bin/wgets'
          if (wgetExists) {
            echo 'Skipping wget installation'
          } else {
            sh "echo 'sudo yum install -y wget'"
          }
          def ChefdkExists = fileExists '/usr/bin/chef-client'
          if (ChefdkExists) {
            echo 'Testing Chef Install...Already installed'
          } else {
            sh 'wget https://packages.chef.io/files/stable/chefdk/4.7.73/el/8/chefdk-4.7.73-1.el7.x86_64.rpm'
            sh 'echo "sudo rpm -ivh chefdk-4.7.73-1.el7.x86_64.rpm" '
          }
        }
      }
    }
  }
}
