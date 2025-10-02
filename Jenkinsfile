node {
   stage('Get the code') { // for display purposes
      // Get some code from a GitHub repository
      sh 'rm -rf ${WORKSPACE}/*'
      sh 'git clone git@gitlab.com:marcochristoforou/stcatherines.git'
   }
   stage('Update website') {
      // Run the maven build
      sh 'scp -r ${WORKSPACE}/stcatherines root@165.22.127.11:/root/www'
   }
   stage('Clear workspace') {
      // Run the maven build
      sh 'rm -rf ${WORKSPACE}/stcatherines'
   }
}
