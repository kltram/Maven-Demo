pipeline {
agent any
stages {
stage ('scm'){
steps {git 'https://github.com/pandian3k/Maven-Demo.git'}
}
stage ('Build'){
steps {bat label: '', script: 'mvn clean'
   bat label: '', script: 'mvn install'}
}
stage ('Deployment'){
steps {bat label: '', script: 'xcopy /y "C:\\Program Files (x86)\\Jenkins\\workspace\\demo-pro\\multi-module\\webapp\\target\\webapp.war" "C:\\Program Files\\Apache Software Foundation\\Tomcat 8.5\\webapps"'}
}
}
}
