def application
def gitrepo
def user
def type
def userId =currentBuild.getBuildCauses()[0].userId


pipeline {
agent any
  options{
timeout(time: 30 , unit: 'MINUTES')
    disableConcurrentBuilds()
  }

  stages{
stage('Source code fetch'){


  steps{
    script {
git branch: 'main', url: 'https://github.com/Ravi-s10/Docker_image_creator.git'



      
    }
  }
}

stage("Read Property file"){


  steps{
script {
prop = readProperties file: "pipeline.properties"
  application=evaluate(prop['application']).toString()
  gitrepo=evaluate(prop['gitRepo']).toString()
  user=evaluate(prop['Username']).toString()
  type=evaluate(prop['Type']).toString()

  echo "Application name is $application"
  echo "Username is $user"
  echo "Type of app is $type"
  echo "Build triggered by $userId"
  echo "Build Branch is ${env.BRANCH_NAME}"

}


    
  }

}
    
stage("Print All"){
    steps{
      script{
        env.each { key,value -> echo "${key} = ${value}"
      }
    }
  }

  

}
}
