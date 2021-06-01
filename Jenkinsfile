pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v $HOME/.m2:/root/.m2'
    }
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean install'
        sh 'cd /var/jenkins_home'
        sh 'mvn -e exec:java -Dexec.mainClass="kpi.acts.appz.bot.hellobot.HelloWorldBot" -Dexec.args="1601078076:AAGTHF43CyPSXfhi209Zd5CkDe56kJpIN4w vagrantbot"'
      }
    }
  }
}

