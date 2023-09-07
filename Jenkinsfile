pipeline {
    agent any
    
    tools{
        jdk 'jdk11'
        maven 'maven3'
    }

    stages {
  
         stage('Package') {
            steps {
                sh "mvn clean package"       

            }
        }
        
         stage('Deploy') {
            steps {
                sh " sudo -S cp target/petclinic.war /opt/apache-tomcat-9.0.65/webapps/ " 

            }
        }
    }
}
