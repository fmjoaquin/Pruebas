node {
    stage('Example') {       
        for (i in [ 'a', 'b', 'c' ]) {
            echo i
         }
    }
    
     stage('Example2') {       
        def userInput = input(
 id: 'userInput', message: 'Let\'s promote?', parameters: [
 [$class: 'TextParameterDefinition', defaultValue: 'uat', description: 'Environment', name: 'env']
])
echo ("Env: "+userInput)
    }
    
    stage('Example3') {       
        echo 'I only execute on the master branch'
    }
}
