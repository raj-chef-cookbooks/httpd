pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'sudo yum update -y'
      }
    }
    /* stage('Install Essential rpms') {
      def wgetExists = fileExists '/bin/wget'
      if (wgetExists) {
        echo 'Skipping wget installation'
      } else {
        sudo yum install -y wget
      }
      def ChefdkExists = fileExists '/usr/bin/chef-client'
      if (chefdkExists) {
        echo 'Skipping Chef Install...Already installed'
      } else {
        sh 'wget https://packages.chef.io/files/stable/chefdk/4.7.73/el/8/chefdk-4.7.73-1.el7.x86_64.rpm'
        sh 'sudo rpm -ivh chefdk-4.7.73-1.el7.x86_64.rpm'
      }
    } */
  }
}
