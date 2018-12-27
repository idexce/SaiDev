node {
        stage('pulling code from git'){
         checkout scm
        }
   stage('Build Image'){
         sh 'sudo docker build -t idexcel-interns/saidev:${BUILD_NUMBER} .'
         sh 'docker tag idexcel-interns/saidev:${BUILD_NUMBER} idexcelinterns/saidev:latest'
   }
   stage('Push Image'){
         sh 'docker login -u idexcelinterns -p kutty170065'
         sh 'docker push idexcelinterns/saidev:latest'
   }
}
