def job = env.BUILD_NUMBER as Integer

def superCoolFunction(success,exit){
    for (i = 0; i <3; i++) {
        echo "in loop result: ${currentBuild.result}"
        if (!success) {
             try {
                    echo "try"
                    sh "exit "+exit
                    return success = true
                    break
                }
             catch (Exception err) {
                    echo "catch"
                }
         }
    }
    echo "superCoolFunction result: ${currentBuild.result}"
}

node {
    def success = false;
    def results = superCoolFunction(success,"1")
    currentBuild.result = (results) ? 'SUCCESS' : 'FAILURE'
    echo "RESULT: ${currentBuild.result}"
}


