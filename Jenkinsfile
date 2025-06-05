pipeline{
 agent any
 tools{
  maven 'Maven'
 }
 stages{
  stage('Checkout') {
   steps{
     git branch: 'master', url: 'https://github.com/Sushma-4123/mav.git'
    }
  }
  stage('Build') {
   steps{
    sh 'mvn clean package'
   }
  }
  stage('Test') {
   steps{
    sh 'mvn test'
   }
  }
  stage('Run Application') {
   steps{
    sh 'java -jar target/MyMavenApp6005-1.0-SNAPSHOT.jar'
   }
  }
}
post{
 success{
  echo 'BUild and deployment successful!'
 }
 failure{
  echo 'Build failed'
 }
}
}

           
