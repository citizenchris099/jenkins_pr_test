def result = 'bad'

def superCoolFunction(){
    for (i = 0; i <3; i++) {
        if (result == 'bad') {
             try {
                    echo "try"
                    return result = 'good'
                } catch (Exception err) {
                    echo "catch"
                    return result = 'bad'
                }
         }
    }
}
node {
    if(superCoolFunction() == 'good'){
        currentBuild.result = 'SUCCESS'
    }else{
        currentBuild.result = 'FAILURE'
    }
    echo "RESULT: ${currentBuild.result}"
}