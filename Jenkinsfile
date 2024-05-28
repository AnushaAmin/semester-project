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
         gcloud compute instances list --zones=us-central1-a
         
         gcloud compute scp /var/lib/jenkins/workspace/project-ToCS_main root@anusha-apache-server:/var/www/html --zone=us-central1-a
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
