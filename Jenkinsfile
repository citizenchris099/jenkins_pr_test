def job = env.BUILD_NUMBER as Integer

def superCoolFunction(){
    def success = false;
    for (i = 0; i <3; i++) {
        echo "in loop result: ${currentBuild.result}"
        if (!success) {
             try {
                    sh "exit 0"
                    success = true
                    break
                }
             catch (Exception err) {
                    echo "catch"
                }
         }
    }
    currentBuld.result = (success) ? 'SUCCESS' : 'FAILURE'
    echo "superCoolFunction result: ${currentBuild.result}"
}

node {
/*
        currentBuild.result = 'SUCCESS'
    try {
        // do something that fails
        sh "exit 1"
        currentBuild.result = 'SUCCESS'
    } catch (Exception err) {
        currentBuild.result = 'FAILURE'
    }
    echo "RESULT: ${currentBuild.result}"

*/

    superCoolFunction()
    echo "RESULT: ${currentBuild.result}"
}


