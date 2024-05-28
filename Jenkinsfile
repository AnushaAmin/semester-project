pipeline {
    
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Application build stage...' 
        }
       }
        stage('Test') {
            steps {
        sh '''         
        gcloud compute scp /var/lib/jenkins/workspace/Semester-Project_main/index.html root@anusha-apache-server:/var/www/html --zone=us-west4-a
        '''
      }
        }
        stage('Run') {
            steps {
                echo 'Application run stage' 
            }
        }
    }
}
