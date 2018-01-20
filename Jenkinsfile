#!groovy 

node {
   stage 'Checkout'
        checkout scm

   stage 'Setup'
        sh 'npm install'
        sh 'npm cache clean -f'
        sh 'npm install -g n'
        sh 'n stable'

   stage 'Mocha test'
        sh "su - ec2-user -c 'npm test'"

   stage 'Cleanup'
        echo 'prune and cleanup'
        sh 'npm prune'
        sh 'rm node_modules -rf'
}

