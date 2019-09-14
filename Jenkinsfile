timestamps{
    node('nodejsoci'){
        
        stage('checkout'){
            checkout scm
            //checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/feitais/PipelineScriptsBackendProject.git']]])
        }
        
        stage('build'){
            sh 'npm install'
        }
        stage('teste'){
            sh 'npm test'
        }
        stage('Code Quality'){
            def sonar = load 'sonar.groovy'
            sonar.codeQuality()
            
        }
    }
}
