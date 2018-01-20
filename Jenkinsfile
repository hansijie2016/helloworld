#!groovy 
node {
   stage 'Checkout'
        checkout scm

   stage 'Setup'
        sh 'npm install'
        sh 'npm cache clean -f'
        sh 'npm install -g n'
        sh 'n stable'
        sh 'npm test'

//   stage 'Mocha test'
//        sh "npm test"

   stage 'Cleanup'
        echo 'prune and cleanup'
        sh 'npm prune'
        sh 'rm node_modules -rf'
}

