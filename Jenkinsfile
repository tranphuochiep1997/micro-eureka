//properties([pipelineTriggers([githubPush()])])

node {
    stage ('Checkout'){
        git branch: 'main', url: 'https://github.com/tranphuochiep1997/micro-eureka.git'
    }

    stage ('Build'){
        sh 'mvn -DskipTests clean package'
        archiveArtifacts '**/target/*.jar'
        echo archiveArtifacts
    }
	
	
    //stage ('Deploy'){
    //    echo 'Hello jenkins deploy stage'
    //}
}    