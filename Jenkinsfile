node{ 
  stage('Git'){ git 'https://github.com/FunnyStori/Simple_BDD_Framework.git' } 
  stage('Run Tests'){ 
    def mvnHome = tool name: 'Maven_PC', type: 'maven' 
                     bat "${mvnHome}/bin/mvn -am -pl autotest-web test -DscreenAfterStep=true" } 
  stage('Report'){ allure includeProperties: false, jdk: '', results: [[path: 'autotest-web/target/allure-results']] 
                 }}
