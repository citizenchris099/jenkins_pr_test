node {
    try {
        // do something that fails
        sh "exit 1"
        currentBuild.result = 'SUCCESS'
    } catch (Exception err) {
         try {
                sh "exit 0"
                currentBuild.result = 'SUCCESS'
            } catch (Exception err2) {
                currentBuild.result = 'FAILURE'
            }
    }
    echo "RESULT: ${currentBuild.result}"
}