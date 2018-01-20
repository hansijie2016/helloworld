#!groovy 

node {
   stage 'Checkout'
        checkout scm

   stage 'Setup'
        sh 'npm install'

   stage 'Mocha test'
        sh 'npm test'

   stage 'Cleanup'
        echo 'prune and cleanup'
        sh 'npm prune'
        sh 'rm node_modules -rf'
}

