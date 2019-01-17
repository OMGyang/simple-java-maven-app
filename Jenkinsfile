pipeline {
    agent {
        docker {
            image 'maven:3-alpine' ##指定maven镜像
            args '-v /root/.m2:/root/.m2' ##设置mavne本地仓库目录
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }

}