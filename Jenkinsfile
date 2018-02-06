node {
    stage('Example') {       
       def abcs = ['a', 'b', 'c']        
        for (i in abcs) {
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
