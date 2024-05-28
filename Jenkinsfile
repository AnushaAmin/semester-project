pipeline {
    
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Application build stage..' 
        }
       }
        stage('Test') {
            steps {
        sh '''
         gcloud compute scp /var/lib/jenkins/workspace/Jenkins-GDC-Demo_main/index.html root@anusha-apache-server:/var/www/html --zone=us-central1-a
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
