mnode {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t exam:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'jbmulei' -p 'Academy@2019' "
sh "docker tag exam:latest jbmulei/exam:latest"
sh "docker push jbmulei/exam:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}
