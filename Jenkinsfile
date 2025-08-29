pipeline {
    agent any
    
    stages {
          // Step 1: Clone the Repository
        stage('Clone Repository') {
            steps {
                // Pull the latest code from the GitHub repository 
                 gitbranch:'main',url:'https://github.com/laxminarayan183/jenkins-github.git'
            }
        }
     // Step 2: Install apache
        stage('apache install') {
            steps {
                sh '''
                 sudo apt update
                 sudo apt install apache2 -y
                 rm /var/www/html/index.html
                 chown -R jenkins:jenkins /var/www/html/index.html
              '''
            }
        }
        
        // Step 3: Deploy the index.html file
        stage('Deploy HTML File') {
            steps {
                sh '''
                # Deploy index.html to the web server directory (e.g. /var/www/html)
                cp index.html /var/www/html/
                '''
            }
        }
    }

}
