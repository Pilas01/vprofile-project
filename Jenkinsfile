pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK17"
    }	
    environment {
        SNAP_REPO = 'maven-snapshots'
        NEXUS_USER = 'nexus'
        NEXUS_PASS = '1be378bc-e89c-421c-84a2-d7c2e6ff4975'
        RELEASE_REPO = 'maven-releases'
        CENTRAL_REPO = 'maven-central'
        NEXUS_IP = '18.191.232.84' 
        NEXUS_PORT = '8081'
        NEXUS_GRP_REPO = 'maven-public'
        NEXUS_LOGIN = 'Nexuslogin'
    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
            
        }
    }        
}
