pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }

    environment {
        SNAP-REPO = 'vprofile-snapshot'
        NEXUS-USER = 'admin'
        NEXUS-PASS = 'admin'
        RELEASE-REPO = 'vprofile-release'
        CENTRAL-REPO = 'vprofile-maven-central'
        NEXUS-GRP-REPO = 'vpro-maven-group'
        NEXUSIP = '172.31.58.94'
        NEXUSPORT = '8081'
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