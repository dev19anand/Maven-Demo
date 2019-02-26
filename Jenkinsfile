pipeline{
    agent any
    stages{
        stage ("SCM"){
        steps {git 'https://github.com/dev19anand/Maven-Demo.git'}
        }
        stage ("build"){
        steps {bat 'mvn clean'
            bat 'mvn install'
        }
        }
        stage ("deploy"){
        steps {bat 'xcopy /y "C:\\Program Files (x86)\\Jenkins\\workspace\\pipeline project\\multi-module\\webapp\\target\\deva.war" "C:\\Program Files\\Apache Software Foundation\\Tomcat 8.5\\webapps"'}
        }
    }
}
