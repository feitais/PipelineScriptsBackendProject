timestamps{
    node('nodejs'){
        def sonar = load “sonar.groovy”
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
            
            sonar.codeQuality()
            
        }
    }
}
