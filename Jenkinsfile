pipeline {
    agent { label 'docker' }
    stages {
        stage('Publish') {
            when {
                branch 'master'
            }
            steps {
              azureUpload blobProperties: [detectContentType: true], containerName: 'fint-personalmappe-policies', filesPath: '**/*.js', storageCredentialId: 'fintdockervolumes', storageType: 'blobstorage'
            }
        }
    }
}
