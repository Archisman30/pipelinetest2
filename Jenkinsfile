pipeline{

node('linux_slave') {

stages{
 stage('SCM'){
 steps{
 echo'Getting the code from git'
 git 'https://github.com/Archisman30/simple-java-maven-app.git'
}
}
 stage('BUILD'){
 steps{
  echo'Building the package'
  sh 'mvn clean package'
}
}
 stage('TEST'){
 steps{
  echo'Testing the code after building'
  sh 'java -jar target/*.jar'
}
}
 stage('ARCHIVE'){
 steps{
 echo'ARCHIVE DONE from local'
 archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
}
}
}
}
}
