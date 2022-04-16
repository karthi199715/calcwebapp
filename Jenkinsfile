node{
    stage('Git Clone'){
        git 'https://github.com/karthi199715/calcwebapp.git'
    }
    stage('Maven Package'){
        def mvnHome = tool name: 'Maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
        sh 'mv /tmp/raja /tmp/rajan'
    }
    stage('Deployment'){ 
        sh 'cp target/*.war /opt/tomcat/webapps'
    }    
}
