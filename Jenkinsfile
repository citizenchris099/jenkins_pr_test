 node {
     stage('Build') {
              checkout scm // <1>
              sh 'echo hello world' // <2>
              dir ('/home/ec2-user/') {
                  sh('test.sh') // <3>
              }
         }
 }