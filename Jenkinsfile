properties([pipelineTriggers([githubPush()])])
node('linux') {
    git url: 'https://github.com/litt4343/infrastructure-pipeline.git', branch: 'master'
    stage('Test') {
        sh "env"
    }
}
