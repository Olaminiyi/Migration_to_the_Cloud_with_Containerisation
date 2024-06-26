

pipeline {
  agent any

  environment {
    REGISTRY_URL = "992382761454.dkr.ecr.us-east-1.amazonaws.com/tooling-ecr"
    AWS_REGION = "us-east-1"
    GIT_REPO_URL = "https://github.com/Olaminiyi/Migration_to_the_Cloud_with_Containerisation.git"
    DOCKER_IMAGE_TAG = "${env.BUILD_NUMBER}" // Using Jenkins build number as the image tagg
  }
  
  stages {

    stage("Initial cleanup") {

      steps {
        dir(path: "${WORKSPACE}") {
          deleteDir()
        }

      }
    }

    stage('Cloning Git') {
      steps {

        checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: env.GIT_REPO_URL]]])
      }
    }
  

    stage('Building image') {
      steps {
        script {
          dockerImage = docker.build "${env.REGISTRY_URL}:${env.DOCKER_IMAGE_TAG}"
        }

      }
    }

    stage('Pushing to ECR') {
      steps {
        script {
          sh "aws ecr get-login-password --region ${env.AWS_REGION} | docker login --username AWS --password-stdin ${env.REGISTRY_URL}"
          sh "docker push ${env.REGISTRY_URL}:${env.DOCKER_IMAGE_TAG}"
        }

      }
    }

    stage('Clean Up') {
      steps {
        cleanWs(cleanWhenAborted: true, cleanWhenNotBuilt: true, cleanWhenUnstable: true, cleanWhenFailure: true)
      }
    }

  }

}


//updated...

