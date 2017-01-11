def job = env.BUILD_NUMBER as Integer

def superCoolFunction(){
    def success = false;
    for (i = 0; i <3; i++) {
        echo "in loop result: ${currentBuild.result}"
        if (!success) {
             try {
                    echo "try"
                    sh "exit 0"
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
    superCoolFunction()
    echo "RESULT: ${currentBuild.result}"
}


