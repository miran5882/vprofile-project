pipeline {
    
	agent any
	
	tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }
	
    environment {
        NEXUS_USER = "admin"
        NEXUS_PASS = "admin"
        NEXUSPORT = "8081"
        NEXUSIP = "54.87.140.148"
        SNAP_REPO = "vprofile-snapshot"
        RELEASE_REPO = "vprofile-release"
	    NEXUS_GRP_REPO = "vpro-maven-group"
        CENTRAL_REPO = "vpro-maven-central"
        NEXUS_LOGIN = "nexuslogin"
        ARTVERSION = "${env.BUILD_ID}"
    }
	
    stages{
        
        stage('BUILD'){
            steps {
                sh 'mvn clean install -DskipTests'
            }

        }
    }       
}    