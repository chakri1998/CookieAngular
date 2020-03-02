node {
        stage('Checkout SCM'){
                git branch: 'master', url: 'https://github.com/chakri1998/CookieAngular.git'
        }
     def project_path="Cookie-Project-Angular/"
        dir(project_path) {
        stage('Install node modules'){
                sh "npm install"
        }
       
        stage('Build'){
                sh "ng build --prod"
        }
        stage('Deploy'){
                sh "pm2 restart all"
        }
        }
}
