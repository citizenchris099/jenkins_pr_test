 node {
     stage('Build') {
              checkout scm // <1>
              sh 'echo hey now' // <2>
              echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL} and the job name = ${env.JOB_NAME} and the workspace
              = ${env.WORKSPACE}" // <3>
         }
 }