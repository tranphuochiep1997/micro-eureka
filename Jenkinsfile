//properties([pipelineTriggers([githubPush()])])

node {
    stage ('Checkout'){
        git branch: 'main', url: 'https://github.com/tranphuochiep1997/micro-eureka.git'
    }

    stage ('Build'){
        sh 'mvn -DskipTests clean package'
        archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true 
        echo artifacts
    }
	
	
    //stage ('Deploy'){
    //    echo 'Hello jenkins deploy stage'
    //}
}    