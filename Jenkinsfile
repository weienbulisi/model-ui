node {
    stage('代码拉取'){
     echo '代码拉取';
     checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '80cdc0d2-dbc3-4705-9396-65d339b5e9da', url: 'https://github.com/weienbulisi/crossgate-gateway.git']]])
    }

    stage('代码构建'){
      bat '''mvn clean install'''
    }

    stage('镜像制作'){
         echo "\033[31m 红任务已执行完成 \033[0m"
         echo "\033[30m 黑任务已执行完成 \033[0m"
         echo "\033[32m 绿任务已执行完成 \033[0m"
         echo "\033[33m 黄任务已执行完成 \033[0m"
         echo "\033[34m 蓝任务已执行完成 \033[0m"
         echo "\033[35m 紫任务已执行完成 \033[0m"
         echo "\033[36m 深绿任务已执行完成 \033[0m"
         echo "\033[37m 白色任务已执行完成 \033[0m"
    }
}
