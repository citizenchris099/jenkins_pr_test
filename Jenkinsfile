def job = env.BUILD_NUMBER as Integer

def superCoolFunction(){
    currentBuild.result = 'FAILURE'
    for (i = 0; i <3; i++) {
        if (currentBuild.result == 'FAILURE') {
             try {
                    if(job<25){
                    echo "made it to if <25"
                    currentBuild.result = 'SUCCESS'
                    }else{
                    echo "made it to else"
                     sh "exit 1"
                    }
                } catch (Exception err) {
                     currentBuild.result = 'FAILURE'
                }
         }
    }
}
node {
    superCoolFunction()
    echo "RESULT: ${currentBuild.result}"
}