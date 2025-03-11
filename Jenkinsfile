pipeline {
    agent any

    environment {
        // 定义环境变量
        EXAMPLE_VAR = 'Hello, World'
    }

    stages {
           stage('Example') {
                steps {
                    script {
                     sh  'echo  "1234"'
                    }
                }
          }
    }

    post {
        success {
            // 构建成功后的操作
            echo 'Pipeline succeeded!'
        }
        failure {
            // 构建失败后的操作
            echo 'Pipeline failed!'
        }
    }
}
