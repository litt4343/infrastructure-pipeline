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
    sh "aws ec2 run-instances --image-id ami-467ca739 --count 1 --instance-type t2.micro --key-name SEIS665 --security-group-ids sg-a3b9c1ea --subnet-id subnet-0d5cb951 --region us-east-1"

    }
}
