properties([pipelineTriggers([githubPush()])])
node('linux') {
    git url: 'https://github.com/litt4343/infrastructure-pipeline.git', branch: 'master'
    stage('Test') {
        sh "env"
    }
}
node ('linux') {
    stage ("GetInstances") {

    sh "aws ec2 describe-instances --region us-east-1"
    }
    stage ("CreateInstance") {
    // TODO

    }
}
