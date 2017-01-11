def job = env.BUILD_NUMBER as Integer

def superCoolFunction(){
    for (i = 0; i <3; i++) {
        if (currentBuild.result == 'FAILURE') {
             try {
                    echo "try"
                    currentBuild.result = 'SUCCESS'
                    break
                }
             catch (Exception err) {
                    echo "catch"
                    currentBuild.result = 'FAILURE'
                }
         }
    }
}

node {
    currentBuild.result = 'FAILURE'
    superCoolFunction()
    echo "RESULT: ${currentBuild.result}"
}