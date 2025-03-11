pipeline {
    agent any

    environment {
        // 定义环境变量
        EXAMPLE_VAR = 'Hello, World'
    }

    stages {
           stage('stage-1') {
                steps {
                    script {
                    echo 'stage-1'
                    bat 'powershell Write-Output "123456"'
                    bat 'powershell Get-Location'
                    bat 'dotnet restore ./HelloJenkins/Hellojenkins.sln '
                    bat "MSBuild.exe ./HelloJenkins/HelloJenkins/Hellojenkins.csproj /p:Configuration=Release"
                    }
                }
          }
                   stage('stage-2') {
                steps {
                    script {
                     echo 'stage-2'
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
