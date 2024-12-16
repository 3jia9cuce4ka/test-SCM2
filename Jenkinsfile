pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM',
                    branches: [[name: '*/main']],
                    doGenerateSubmoduleConfigurations: false,
                    submoduleCfg: [],
                    userRemoteConfigs: [[
                        url: 'https://github.com/3jia9cuce4ka/test-SCM.git',
                        credentialsId: 'github'
                    ]]
                ])
            }
        }
    }
    triggers {
        pollSCM('H/1 * * * *')
    }
}