 node {
     stage('Build') {
              checkout scm // <1>
              sh 'echo hey now' // <2>
              echo "the workspace = ${env.WORKSPACE}" // <3>
              dir ('/home/ec2-user/') {
                  sh('./test.sh')
              }
         }
 }