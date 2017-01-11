def superCoolFunction(){
    for (i = 0; i <3; i++) {
        if (currentBuild.result == 'FAILURE') {
            echo "count = : ${i}"
            echo "RESULT: ${currentBuild.result}"
         }
    }
}
node {
    try {
        currentBuild.result == 'FAILURE'
        superCoolFunction()
    } catch (Exception err) {
         currentBuild.result = 'FAILURE'
    }
    echo "RESULT: ${currentBuild.result}"
}