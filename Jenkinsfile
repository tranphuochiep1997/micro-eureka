//properties([pipelineTriggers([githubPush()])])

node {
    stage ('Checkout'){
        git branch: 'main', url: 'https://github.com/tranphuochiep1997/micro-eureka.git'
    }

    stage ('Build'){
        sh 'mvn -DskipTests clean package'
        sh 'cp target/*.jar /home/tranphuochiep1997/build/'
        sh 'ls /home/tranphuochiep1997/build'
    }
	
	
    //stage ('Deploy'){
    //    echo 'Hello jenkins deploy stage'
    //}
}    