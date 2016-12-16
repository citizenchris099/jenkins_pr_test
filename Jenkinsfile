 node {
     stage('Build') {
              checkout scm // <1>
              sh 'echo hey now' // <2>
              echo "the workspace = ${env.WORKSPACE}" // <3>
              sh 'echo what the deal' // <4>
              sh ('testScript.sh') // <5>
         }
 }