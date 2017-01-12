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
    return success
}

node {
    def result = false
    result = superCoolFunction("1")
    if(result == true){
    echo "made it to if"
    result = superCoolFunction("1")
    }
    echo "RESULT: ${currentBuild.result}"
    currentBuild.result = (result) ? 'SUCCESS' : 'FAILURE'
    echo "superCoolFunction result: ${currentBuild.result}"
}


