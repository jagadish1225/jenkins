// pipeline {
//     agent any
//     parameters {
//         string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

//         text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

//         booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

//         choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

//         password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
//     }
//     stages {
//         stage('Example') {
//             steps {
//                 echo "Hello ${params.PERSON}"

//                 echo "Biography: ${params.BIOGRAPHY}"

//                 echo "Toggle: ${params.TOGGLE}"

//                 echo "Choice: ${params.CHOICE}"

//                 echo "Password: ${params.PASSWORD}"
//             }
//         }
//     }
// }

pipeline{
    agent any

    parameters{
        choice(name: 'ENV', choices: ['DEV', 'PROD'], description: 'choose ENV')
    }
    stages{
        stage ('DEV'){
             when {
            
                environment name: 'ENV', value: 'DEV'
            }
            steps {
                echo 'DEV'
            }
        }
        tage ('PROD'){
             when {
            
                environment name: 'ENV', value: 'PROD'
            }
            steps {
                echo 'PROD'
            }
        }

        
    }
}
