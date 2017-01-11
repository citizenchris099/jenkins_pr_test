def job = env.BUILD_NUMBER as Integer

def superCoolFunction(){
    currentBuild.result = 'FAILURE'
    for (i = 0; i <3; i++) {
        if (currentBuild.result == 'FAILURE') {
             try {
                    echo "try"
                    currentBuild.result = 'SUCCESS'
                } catch (Exception err) {
                    echo "catch"
                    currentBuild.result = 'FAILURE'
                }
         }
    }
}
node {
    superCoolFunction()
    echo "RESULT: ${currentBuild.result}"
}