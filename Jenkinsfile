#!groovy 

node {
   stage 'Checkout'
        checkout scm

   stage 'Setup'
        sh 'sudo npm install'

   stage 'Mocha test'
        sh './node_modules/mocha/bin/mocha'

   stage 'Cleanup'
        echo 'prune and cleanup'
        sh 'sudo npm prune'
        sh 'sudo rm node_modules -rf'
}

