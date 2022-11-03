pipeline {
    agent {label "lastslave"}
    

    stages 
    {
        stage('git checkout') 
        {
            steps {
   
                git 'https://github.com/aya-ibrahim-m/grad-project-ci-cd-node.js-app.git'
            }
        }
        
        stage('build') {
            steps {
                sh 'docker build -f dockerfile . -t gcr.io/iti-1-366311/nodejs:latest'
            }
        }
        
        stage('artifact') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'gcr')]){
                sh 'gcloud auth configure-docker'
                sh 'docker tag nodejs gcr.io/iti-1-366311/nodejs'
                sh 'docker push gcr.io/iti-1-366311/nodejs:latest'
            }                                                       
           }
        }
        
        stage('deloy') {
            steps 
            {

                #sh 'kubectl create namespace my-app'
                sh 'kubectl apply -f ./app-deployment.yaml -n my-app'
                sh 'kubectl apply -f ./app-service.yaml -n my-app'
                
            }
           }
        }
}
