code for pipeline  (jenkins file)
node('master') {
    stage('continuous download') {
    git 'https://github.com/selenium-saikrishna/maven.git'
}
stage('continuous build') {
    sh label: '', script: 'mvn 

package'
}
stage('continuous deploy') {
   sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/pipeline1/webapp/target/webapp.war 

ubuntu@172.31.34.68:/tmp/buildfile123.war'
}
stage('continuous testing') {
    git 'https://github.com/selenium-saikrishna/FunctionalTesting.git'
    sh label: '', script: 

'''java -jar /home/ubuntu/.jenkins/workspace/pipeline1/testing.jar
'''
   
}
stage('continuous delivery') {
    input message: 'waiting for DM to approve further', 

submitter: 'srinivas'
    sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/pipeline1/webapp/target/webapp.war ubuntu@172.31.40.21:/tmp/buildfile123.war'
}

}
