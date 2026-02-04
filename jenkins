pipeline {
    agent any
    environment{
    name = 'Rohit' 
}
parameters {
    string(name: 'Person', defaultValue: 'Raja', description: "Who are you?")
     booleanParam(name: 'isMale', defaultValue: true, description: "")
choice(name: 'City', choices: ['Jaipur','Mumbai','Pune'], description: "")
}
    stages {
        stage('Parameters') {
            steps {
                sh 'echo "${Person}"'
                sh '''
                ls 
                date
                pwd 
                '''          
                  }
                }
        stage('Environment variable') {
            
             environment{
              uname = 'Mandal' 
               }
             steps {
                sh 'echo "${Person}"'
                sh 'echo "${name}"'
            }
        }      
        stage('Continue ?') {
            input {
                 message "Should we continue?"
                 ok "Yes we Should"

                  }
            steps {
                sh 'echo "${uname}"'
                echo 'Deploy'
            }
   
        }
      stage('Deploy on test') {
            steps {
                sh 'echo "${uname}"'
                echo 'Deploy'
            }
   
        }

    }
post{
   always { 
            echo 'I will always say Hello again!'
        }
}
}
