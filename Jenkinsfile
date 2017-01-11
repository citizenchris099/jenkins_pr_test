def job = env.BUILD_NUMBER as Integer

def superCoolFunction(){
    for (i = 0; i <3; i++) {
        echo "in loop result: ${currentBuild.result}"
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
    echo "exit result: ${currentBuild.result}"
}

node {
    currentBuild.result = 'FAILURE'

    for (i = 0; i <3; i++) {
        echo "in loop result: ${currentBuild.result}"
        if (currentBuild.result == 'FAILURE') {
             try {
                    echo "try"
                    currentBuild.result = 'SUCCESS'
                    echo "in loop result: ${currentBuild.result}"
                    break
                }
             catch (Exception err) {
                    echo "catch"
                    currentBuild.result = 'FAILURE'
                }
         }
    }

//    superCoolFunction()
    echo "RESULT: ${currentBuild.result}"
}