pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                retry(3){
                    withAWS(region:'us-west-2', credentials:'aws-static'){
                    s3Upload(file:'index.html', bucket:'ahmed-abdallah-jenkins', path:'')
                }                             
            }
        }
        // stage('Build') {
        //     steps {
        //         sh 'echo "Hello World"'
        //         sh '''
        //             echo "Multiline shell steps works too"
        //             ls -lah
        //         '''
        //     }
        // }
    }
}