import groovy.json.JsonSlurperClassic

def jsonParse(def json){
 new groovy.json.JsonSlurperClassic().parseText(json)
}
pipeline{
 agent any
 environment{ appName="variable"}
 stages{
  stage("paso 1"){
   steps{
     script{sh "hola mundo"}
   }
  }
 }
 post{
  always{
   
   sh "echo 'fase always'"
  }
  success{
   sh " echo 'fase success'"
  }
  failure{
    sh "echo 'fase failure'"
  }
 }
}
