pipeline {
  agent {label 'Jenkins-agent'}
  tools {
    jdk 'Java17'
    maven 'Maven3'
  }
  stages {
    stage ("check out for SCM"){
    steps {
      git branch: 'main', credentialsId: 'github', url: 'https://github.com/santhoshi254/register-app.git'
    }
    }
    stage ("Build Application"){
      steps {
        sh "mvn clean package"
      }
    }
    stage ("Test Application"){
      steps {
        sh "mvn test"
      }
    }
  }
}
