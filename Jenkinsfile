node {
    stage('代码拉取'){
     echo '代码拉取';
     checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '80cdc0d2-dbc3-4705-9396-65d339b5e9da', url: 'https://github.com/weienbulisi/crossgate-gateway.git']]])
    }

    stage('代码构建'){
      bat '''mvn clean '''
      bat '''mvn clean install'''
    }

    stage('项目启动'){
      bat '''dir'''
      bat '''cd C:\\Windows\\system32\\config\\systemprofile\\AppData\\Local\\Jenkins\\.jenkins\\workspace\\test\\target'''
      bat '''dir'''
      bat '''docker build -t test:v1.2.6 .'''
      echo "启动程序成功"
    }

}
