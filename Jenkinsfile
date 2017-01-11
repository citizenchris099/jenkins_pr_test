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

        currentBuild.result = 'START'
    try {
        // do something that fails
        sh "exit 0"
        currentBuild.result = 'SUCCESS'
    } catch (Exception err) {
        currentBuild.result = 'FAILURE'
    }
    echo "RESULT: ${currentBuild.result}"

/*
//    currentBuild.result = 'FAILURE'

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
    */
}


