pipeline{

agent any

stages{
 stage('SCM'){
 steps{
 git 'https://github.com/Archisman30/simple-java-maven-app.git'
}
}
 stage('BUILD'){
 steps{
  sh 'mvn clean package'
}
}
 stage('TEST'){
 steps{
  sh 'java -jar target/*.jar'
}
}
 stage('ARCHIVE'){
 steps{
 sh 'target/*.jar'
}
}
}
}
