def superCoolFunction(){
    for (i = 0; i <3; i++) {
        if (currentBuild.result == 'FAILURE') {
            echo "count = : ${i}"
            echo "RESULT: ${currentBuild.result}"
         }
    }
}


node {
    currentBuild.result == 'FAILURE'
    try {
        superCoolFunction()
    } catch (Exception err) {
         currentBuild.result = 'FAILURE'
    }
    echo "RESULT: ${currentBuild.result}"
}