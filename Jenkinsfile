//properties([pipelineTriggers([githubPush()])])

node {
    stage ('Checkout'){
        git branch: 'main', url: 'https://github.com/tranphuochiep1997/micro-eureka.git'
    }

    stage ('Build'){
        sh 'mvn -DskipTests clean package'
    }
	
    stage ('Deploy'){
    	echo 'jar file: ${env.WORKSPACE}/target/eureka-0.0.1-SNAPSHOT.jar'
    	sh 'ansible-playbook -i /etc/ansible/hosts deploy-playbook.yml -e "JAR_FILE=${env.WORKSPACE}/target/eureka-0.0.1-SNAPSHOT.jar"'
    }
}    