def job = env.BUILD_NUMBER as Integer

def superCoolFunction(exit){
    def success = false;
    for (i = 0; i <3; i++) {
        echo "in loop result: ${currentBuild.result}"
        if (!success) {
             try {
                    echo "try"
                    sh "exit "+exit
                    success = true
                    break
                }
             catch (Exception err) {
                    echo "catch"
                }
         }
    }
    currentBuild.result = (success) ? 'SUCCESS' : 'FAILURE'
    echo "superCoolFunction result: ${currentBuild.result}"
}

node {
    stage('Build') {
        superCoolFunction("1")
        echo "RESULT: ${currentBuild.result}"
        }
    }
}


