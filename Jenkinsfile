pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }
    environment {
        SNAP_REPO = 'fidevops-snapshort'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'admin123'
        RELEASE_REPO = 'fidevops-release'
        CENTRAL_REPO = 'fidevops-maven-central'
        NEXUSIP = '172.31.50.80'
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = 'fidevops-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}