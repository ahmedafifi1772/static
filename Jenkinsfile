pipeline {
  agent any 
  stages {
     stage('Upload to AWS') {
          steps {
              withAWS(region:'eu-central-1',credentials:'jenkins-blueocean') {
                s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html', bucket:'onemorestore')
              }
          }
     }
  }
}