def application
def gitrepo
def user
def type

pipeline {
agent any

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
  username=evaluate(prop['Username'])
  type=evaluate(prop['Type'])

  echo "Application name is $application"
echo "Username is $Username"
  echo "Type of app is $Type"

}


    
  }

}












    
  }

  

}
