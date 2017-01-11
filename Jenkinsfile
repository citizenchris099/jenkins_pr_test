def job = env.BUILD_NUMBER as Integer

def superCoolFunction(){
    currentBuild.result = 'FAILURE'
    for (i = 0; i <3; i++) {
        if (currentBuild.result == 'SUCCESS') {
             try {
                    echo "try"
                    sh "exit 1"
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