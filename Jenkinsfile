code for pipeline  (jenkins file)
node('master') {
    stage('continuous download_loans') {
    git 'https://github.com/selenium-saikrishna/maven.git'
}
stage('continuous build_loans') {
    sh label: '', script: 'mvn 

package'
}
stage('continuous deploy_loans') {
   sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/pipeline1/webapp/target/webapp.war 

ubuntu@172.31.34.68:/tmp/buildfile123.war'
}

}
