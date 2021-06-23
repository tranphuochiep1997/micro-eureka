//properties([pipelineTriggers([githubPush()])])

node {
    stage ('Checkout'){
        git branch: 'main', url: 'https://github.com/tranphuochiep1997/micro-eureka.git'
    }

    stage ('Test'){
        echo 'Hello jenkins edit 2003'
    }
	
	
    //stage ('Deploy'){
    //    echo 'Hello jenkins deploy stage'
    //}
}    