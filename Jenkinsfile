pipeline{
    agent any
    stage('build da imagem docker'){
        steps{
            sh 'docker build -t devops/app .'
        }
    }
    stage('build subir o docker compose - redis e app'){
        steps{
            sh 'docker-compose up --build -d'
        }
    }
    stage('sleep para subida de containers'){
        steps{
            sh 'sleep 10'
        }
    }
    stage('teste da aplicaçao'){
        steps{
            sh 'teste-app.sh'
        }
    }
}